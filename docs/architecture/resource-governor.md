# Resource governor and execution throttle

Status: authorized design addition; runtime enforcement is not implemented. Numerical settings below are an illustrative pilot policy, not measured optimal values or active defaults. No model provider, framework, or hosting platform is selected.

## Purpose and ownership

The Career Orchestrator decides which work is useful. A resource governor in the future orchestration software decides whether that work may start within the configured limits. Prompt instructions alone do not enforce resource bounds.

The governor is a runtime component, **not a tenth agent**. All nine career agents retain their separate contracts. Limits apply to executing instances and calls, not to whether an agent remains part of the architecture. Invoke only relevant agents and queue additional work when capacity is full.

The [model hierarchy](model-routing.md) places central orchestration on a frontier-capability model and routine specialists on inexpensive qualified models. It selects worker targets from measured evidence, not from this governor's hard ceilings. Frontier escalations remain specialist instances and consume the same root allowances and capacity. No model substitution may bypass pricing, data permissions, retry/review limits, or required human decisions.

## Scope and invariants

One root workflow ID covers the user's bounded objective, every specialist task, any delegated work, orchestration calls, critiques, revisions, retries, model calls, and tool calls. All descendants use the same budget ledger and policy version. Creating a child task, restarting a process, or resuming a checkpoint cannot reset counters or create a fresh allowance.

Only the nine approved career roles may receive tasks. Agents cannot spawn extra agent types or unbounded copies of themselves. Every executing instance must be registered and admitted. Waiting or idle role definitions consume no worker slot; orchestration model calls do consume capacity. A parent that waits for a child releases its active execution slot only when it has no in-flight operation.

Hard limits protect capacity, call counts, tokens, time, and configured spend. Efficiency rules reduce unnecessary work. Neither category can override evidence standards, critical review, hard career constraints, privacy, or action approvals.

## Illustrative pilot policy

The [synthetic policy example](../../examples/synthetic/resource-policy.json) expresses these settings as non-executable reference data. Select and version an actual policy before governed execution. These values are not claims about model context sizes, provider quotas, or task completion guarantees.

| Control | Illustrative value | Counting rule / effect |
| --- | --- | --- |
| Agent roster | Original nine roles | Any other role is rejected pending an approved architecture change |
| Concurrent workers | 3 per root workflow | Count every registered executing instance, including active orchestration; queue excess work |
| Model calls | 24 per root workflow | Count each outbound attempt, including orchestration, critiques, and retries |
| Tool calls | 12 per root workflow | Count each outbound attempt, including retries; zero-cost tools still count |
| Aggregate model tokens | 60,000 per root workflow | Count input plus output usage across all calls, including billed reasoning where applicable |
| Input allowance per model call | 12,000 tokens | Include instructions, selected context, evidence, and message history |
| Output allowance per model call | 2,000 tokens | Bound generated output with a supported provider limit; include other billed generation in reservations |
| Retry limit | 1 retry per task | At most two task attempts; both share original IDs, counters, and deadlines |
| Review/revision limit | 2 additional rounds per artifact lineage | Count after initial draft/review; renaming an artifact cannot restart the allowance |
| No-progress limit | 2 consecutive non-progress review/revision rounds | Pause when neither produces material evidence, resolves a gap, nor corrects a defect |
| Model/tool call timeout | 90 seconds | Request cancellation and reconcile any uncertain usage or action result |
| Task timeout | 300 seconds | Elapsed time from first dispatch, including retries; no reset between attempts |
| Workflow execution time | 900 seconds | Accumulate running/draining elapsed time across resumes; exclude genuine paused user-wait time |
| Monetary budget | Must be selected before governed execution | Amount, currency, pricing version, and relevant tool fees are required; no assumed free execution |

Each task may have tighter limits. Task allowances draw from the root allowance rather than adding to it. A stricter deployment or service-wide ceiling takes precedence. A multi-workflow deployment must also set service-wide concurrency and aggregate spending limits so many individually bounded workflows cannot overload the service.

The illustrative three-instance concurrency ceiling does not recommend three workers. The policy field `concurrent_workers` counts all executing instances, including active orchestration. Apply any measured specialist-worker target as an additional bound; active orchestration plus admitted specialists must still fit the total ceiling. More expensive frontier-specialist routes count as workers too. The [model-routing reference](../../examples/synthetic/model-routing-policy.json) leaves the production target unset pending qualifying trials.

## Admission and accounting

Before admitting an instance or issuing a model/tool request, the runtime must:

1. Check that the root workflow is running, its policy is valid, the role is allowed, dependencies are satisfied, and the task is neither cancelled nor duplicated.
2. Check action authorization separately. Available budget never grants permission to send, submit, or share information.
3. Estimate conservative token and monetary upper bounds for the request using the selected provider's accounting and current recorded prices. Include input, maximum billed generation, and applicable tool fees. If an upper bound cannot be established, block governed execution of that operation; do not treat unknown cost as zero.
4. Atomically check and reserve capacity and budget against the shared ledger, including all outstanding reservations. Concurrent workers cannot each spend the same remaining allowance.
5. Before dispatch, commit a unique operation ID and charge the appropriate call-attempt counter. A model-triggered tool operation is separately admitted; count both the model and tool requests where both occur.
6. Reconcile the reservation with reported usage and actual result. Release only confirmed unused reservations, and release execution capacity only when the operation is confirmed stopped. An admitted request cancelled before dispatch may release its reservation without consuming an outbound-attempt count.

Counters and reservations must survive process failure. An unresolved request retains a conservative reservation until reconciled. Do not assume that a timeout means no billing or no external action occurred, and do not dispatch a replacement worker while its predecessor may still be running. A provider refusal or transport retry still consumes an outbound-attempt count if a request was issued.

Resolve the actual model/provider/version and price basis on every dispatch, including escalation. Reserve against that route's cost rather than the original worker's cheaper rate. Record usage by route/model as well as root totals so supervision overhead and savings claims can be evaluated. Selecting a qualified model route never creates a separate budget.

Token and spend admission bounds depend on provider limits, known prices, and complete accounting. Unexpected metering or price differences must be recorded, halt further dispatch, and trigger reconciliation. Do not claim guaranteed invoice-level precision when actual usage is delayed or incomplete.

For manual role-play without reliable metering, record usage as unavailable and label the exercise **advisory**, not resource-governed. It cannot be presented as enforced autonomous execution. The reference JSON deliberately leaves monetary settings unset and must not be activated as-is.

## Efficiency rules

- **Relevant-agent routing:** preserve all nine roles, invoking only those needed for the current objective.
- **Duplicate detection:** identify work using objective, opportunity/source identity, ontology version, evidence versions, artifact/payload version, and access scope. Check queued and running tasks as well as completed results.
- **Safe reuse:** reuse a result only when its inputs, permissions, and source freshness are still valid. Reuse of an approved draft does not authorize a new send. Keep private cache entries isolated by user/access scope.
- **Selective context:** provide task-relevant facts, reasons, and evidence rather than the entire career corpus. Never trim away material constraints, contrary evidence, or approval boundaries just to fit the allowance; pause or split the task within the same root budget.
- **Bounded review:** a round must cite new evidence, an identified correction, or an unresolved material issue. Longer text and agent agreement alone do not count as progress.
- **Quality-aware scheduling:** prioritize required critique and validation when allocating remaining work. If the remaining allowance cannot support a complete review, return a partial packet with the missing checks explicitly identified.

## Limit handling and recovery

Workflow states are proposed as running, draining, paused, completed, failed, and cancelled. A queue-capacity event normally delays a task without pausing the whole workflow. A budget, attempt, time, or no-progress limit stops new dispatch and records the reason.

On a hard stop, enter draining, request cancellation of unnecessary in-flight work, and preserve reservations until operations are resolved. Work already issued may still consume its reserved resources. Once in-flight operations are settled, checkpoint and pause. A timeout with an unknown send result also enters reconciliation; it never justifies an automatic resend.

The checkpoint includes root/task/operation IDs, policy version, ontology/input versions, completed artifacts, remaining tasks, critic/review status, consumed usage, outstanding reservations, active operations, limit reason, and the next decision. Required critique or authorization that was not completed remains incomplete. A partial packet cannot be labeled a verified final recommendation.

Resume with the same ledger, elapsed-time accumulator, retry counts, and artifact lineage. A user-authorized limit adjustment creates a new policy version and records old/new limits and why; it does not erase spend or remove service-wide ceilings. No agent may raise its own limits, fork a new root objective to evade a limit, silently change models to escape accounting, or claim an approval that was not given.

## Records and verification

Maintain a private ledger of requested/admitted/queued/blocked/completed operations, timestamps, policy/input versions, reservations, actual usage or uncertainty, retries, stop reasons, and user-authorized changes. Keep private prompt bodies and candidate information out of public telemetry.

Use the [resource-budget record](../../templates/resource-budget.md) and [agent handoff](../../templates/agent-handoff.md). Report peak concurrency, model/tool attempts, tokens, spend and accounting uncertainty, duplicate work avoided, review rounds, no-progress stops, and remaining work alongside quality measures.

Requirements HS-017 through HS-020 and scenarios EV-17 through EV-24 cover the intended behavior. They are not executed tests. See [traceability](../../aidlc-docs/inception/traceability.md) and [acceptance scenarios](../../evaluation/acceptance-scenarios.md).
