# Model hierarchy and evidence-led worker scaling

Status: authorized architecture direction; no model routing or agent runtime is implemented. Specific providers, model IDs, prices, quality thresholds, and production worker counts remain unselected.

## Architecture principle

Use a frontier-capability model for the central Career Orchestrator and inexpensive, task-qualified models for routine specialist work. Measure the value of additional executing workers before selecting a worker count. Capability, evidence quality, total cost, and useful latency determine routing and capacity decisions; a headline agent count is not a target.

The expected economic advantage is a hypothesis to evaluate. A low worker token price can be outweighed by supervision, repeated context, retries, poor outputs, or consolidation. Frontier status alone is also not proof that a particular model meets this project's quality requirements.

## Roles, models, and instances are different

| Concept | Meaning | What may vary |
| --- | --- | --- |
| Agent role | One of the nine career responsibilities and contracts | Roster changes require a separate approved architecture decision |
| Model tier | Selected model capability/cost class used for a task | Route according to approved policy and measured task performance |
| Executing instance | A registered worker doing a bounded task under a role | Several instances may serve independent tasks, within measured targets and governor ceilings |
| Concurrency target | Permitted simultaneous specialist execution for a workload class | Selected only from a validated, policy-authorized scaling envelope |
| Hard resource ceiling | Governor's maximum admitted instances, calls, tokens, cost, and time | Cannot be raised by agents or bypassed by model routing |

The Career Orchestrator is one central coordination role. The other eight roles remain distinct even if they share one inexpensive model. An escalated specialist task remains owned by its original role; using a frontier model does not merge that role into the orchestrator.

## Default routing direction

These tier assignments define the intended hierarchy. Actual model assignments require task-specific evaluation, tool support, authorized data processing, and a recorded pricing basis.

| Agent | Intended default tier | Work assigned / escalation boundary |
| --- | --- | --- |
| Career Orchestrator | Frontier | Interpret the objective, plan bounded tasks, select routes, reconcile conflicts, and synthesize a review packet |
| Career Ontology | Economy for routine proposals | Extract and link supported records; escalate contradictory evidence or complex semantic changes; user confirmation rules still apply |
| Job Market Intelligence | Economy | Inspect listings, extract requirements, deduplicate, and record freshness; escalate ambiguous evidence rather than invent facts |
| Job Fit Analysis | Economy | Apply approved criteria and map evidence; escalate unresolved material tradeoffs or contradictions |
| Resume Strategy | Economy | Draft from approved claims; escalate unresolved strategy questions without inventing experience |
| Recruiter & ATS Analysis | Economy | Compare stated requirements and terminology; escalate ambiguous screening interpretation |
| Interview Preparation | Economy | Build supported stories and role-specific practice; escalate complex cross-source reasoning |
| Networking | Economy | Prepare recipient context and message drafts; uncertain identity or missing permission requires verification/user input, not merely a stronger model |
| Critical Reasoning | Economy for initial independent assessment | Inspect evidence and defects; escalate material disputes or failed quality checks to a frontier-capability model when policy and budget permit |

Deterministic parsing, validation, and arithmetic should use ordinary software when appropriate. They do not require additional AI agents. Critical review remains a separate task/context even when its escalated model is also used by the orchestrator; record the actual independence and model identity rather than claiming a different model or independent service was used.

## Model registry and dispatch contract

An actual runtime must resolve each tier to an approved registry entry: provider; exact model/version; allowed task types and tools; context/output capabilities; data/privacy authorization; measured evaluation results; and dated prices for all billed usage. Credentials remain outside prompts and public files.

Before dispatch, the orchestrator records task/role, complexity and material uncertainty, chosen tier/model version, route reason, ontology/input versions, expected validation, and the shared resource-policy reference. The runtime validates the route and the [governor](resource-governor.md) admits the operation using that model's accounting. All worker, orchestration, critique, retry, and escalation costs share the same root ledger.

If the intended model is unavailable, unqualified, unpriced, or unauthorized for the data, pause the affected task or use an explicitly permitted and qualified route. Do not silently replace a required frontier orchestration route with an inexpensive model, switch providers with different data permissions, or use an escalation to escape accounting. A single-model manual exercise remains useful but must be labeled as simulation of the architecture rather than deployed tiered execution.

## Escalation and review

1. Apply deterministic checks and the role's evidence/output contract to the worker result. Passing a schema check alone does not prove factual or reasoning quality.
2. For a material ambiguity, conflict, or failed quality check, record the issue and the smallest useful escalation objective. Model confidence or verbosity alone does not justify escalation.
3. Check whether the missing input is factual, user-specific, or a permission issue. A stronger model cannot supply absent evidence, confirm a user's preference, or authorize outreach; mark the task blocked or ask for the missing input when necessary.
4. Route a suitable reasoning problem to the frontier tier only within allowed routes and the same root budgets. A retry/revision escalation uses the existing attempt/revision allowance; it does not receive a new task budget or reset lineage.
5. Preserve the worker result, escalation reason, actual route, critique, corrections, and unresolved dissent. The orchestrator consolidates the result while required user decisions remain open.

Do not routinely run every specialist result through a full frontier rewrite. Use bounded validation and targeted review, and measure frontier supervision as part of total system overhead. Required critique and approval cannot be dropped to make the hierarchy appear inexpensive.

## Choosing worker counts

Begin measurement with one executing specialist worker as a serial comparison baseline; that is not a claimed production optimum. Keep the production target unset until there is qualifying evidence. The [worker-scaling protocol](../../evaluation/worker-scaling.md) compares repeated runs of the same workload at different allowed concurrency levels.

Worker count means simultaneous specialist instances, including frontier-escalated specialists. Active orchestration also consumes governor capacity. For example, under the existing illustrative ceiling of three total executing instances, two specialists plus one active orchestrator fill capacity. That arithmetic does not select two workers as optimal. The governor's reference ceiling is a safety bound, not a performance recommendation.

Evaluate only independent tasks with satisfied dependencies and pinned inputs. Do not parallelize unsynchronized ontology writes, approvals, or dependent stages. An orchestrator bottleneck or lack of ready work can eliminate the benefit of another worker.

A measured scaling record must identify the workload class, models, routing/resource-policy versions, baseline/candidate counts, sample size, quality results, complete-work denominators, total cost, latency, and overhead. Predeclare what benefit matters and the maximum acceptable tradeoff before selecting a candidate. Quality and permission gates always apply; production tuning requires a validated envelope permitted by the operating policy.

Within that envelope, a future orchestrator may request a higher or lower target based on ready independent work and measured results. The governor makes admission decisions and may impose a lower count. No evidence, no valid target, or no meaningful measured gain means no scale-up. Increasing a hard ceiling or changing authorization still requires the existing policy-change process.

## Reference artifacts and open choices

The [model-routing example](../../examples/synthetic/model-routing-policy.json) is non-executable reference data. It leaves provider/model IDs, production worker target, scaling evidence, and decision thresholds unset. It cannot activate a runtime or demonstrate cost savings. The separate [governor example](../../examples/synthetic/resource-policy.json) still provides only illustrative safety ceilings.

Use the [scaling experiment record](../../templates/scaling-experiment.md), [handoff template](../../templates/agent-handoff.md), and [scorecard](../../evaluation/scorecard.md). Requirements HS-021 through HS-023 and scenarios EV-25 through EV-30 define intended coverage, not passing runtime results.
