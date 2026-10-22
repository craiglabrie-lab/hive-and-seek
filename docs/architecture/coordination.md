# Coordination and handoff protocol

Status: proposed contract for manual and future automated execution.

## Dispatch

The orchestrator creates a task with a unique task ID, one owner, objective, required inputs, approved ontology version, allowed tools, output contract, dependencies, and effort limit. Each task carries its root workflow ID, resource-policy version, and shared budget-ledger reference. The task ledger prevents duplicate work by checking opportunity/source identity, objective, input versions, and access scope before assignment. Future runtime execution must pass the [resource governor](resource-governor.md) before starting an instance or issuing a model/tool request.

All roles use the [handoff template](../../templates/agent-handoff.md). Artifacts include task ID, actor, timestamps, source references, and ontology version. A manual pilot can maintain this in Markdown; no task engine currently exists.

Use the [model hierarchy](model-routing.md): frontier-capability central orchestration, inexpensive qualified routine workers, and bounded specialist escalation. Record the chosen tier/model/version and why, including whether a task is missing evidence rather than requiring stronger reasoning. All nine responsibilities remain separate regardless of how models are shared.

Proposed task states: queued → running → ready-for-review → completed. A task may instead be paused, blocked, failed, or cancelled. A blocked task names its missing input; a paused task names its resource or user-decision boundary. A retry keeps the original task ID and adds an attempt number; it does not silently create a second task or reset the root allowance.

## Shared knowledge

Roles read a pinned ontology snapshot. Only the ontology role proposes changes to shared career knowledge, using an [ontology change record](../../templates/ontology-change.md). New preferences and changed hard constraints require user confirmation. The orchestrator checks whether a newer snapshot affects open tasks; affected outputs are revalidated or marked stale.

User corrections supersede inferences. Conflicting evidence is preserved with source references. A confidence label is an assessment, not a calibrated probability.

## Independent challenge

The critic receives the task question, criteria, and evidence before seeing the recommendation where practical. Record an initial independent assessment, then compare it with the recommendation. A critic simulated by the same model is labeled as such; stronger independence is a future runtime option.

The critic checks unsupported claims, missing constraints, desirability/capability conflation, stale sources, and plausible alternative interpretations. The orchestrator resolves factual disputes from evidence and asks the user about unresolved preference disputes. Neither a vote nor a majority overrides a hard constraint. Material dissent remains visible in the final packet.

## Consolidation

A completed packet contains sources and freshness, capability assessment, desirability assessment, uncertainty, constraint results, recommendation, draft material, critique and response, and the next action. The user sees a concise result with access to the underlying records.

## External actions and recovery

The initial pilot is draft-only. A future tool-enabled action needs permission tied to the recipient or destination, exact payload version, and action. Recheck permission and payload immediately before execution; changes invalidate the approval. Record the actual service result. If delivery status is unknown, reconcile it before retrying to avoid duplicate submissions or messages.

A bounded retry policy, concurrency limit, timeout, and token/cost budget must be chosen before autonomous execution. The [resource-governor specification](resource-governor.md) defines aggregate admission, accounting, no-progress stops, safe reuse, cancellation, and recovery. Its [reference policy](../../examples/synthetic/resource-policy.json) is illustrative and not active configuration. Parallelism is appropriate for independent evidence collection or critique, not unsynchronized writes to shared preferences or approvals.

All nine roles remain defined even when execution is throttled. Required critique and approval remain incomplete when resources run out; do not silently omit them or label a partial packet verified. Checkpoints preserve usage counters, elapsed time, retry/revision history, in-flight operations, reservations, and versions. Resume revalidates inputs and uses the same ledger. An unknown external-action result must be reconciled before retry, regardless of remaining budget.

Worker scaling needs a workload/model-specific [measurement record](../../templates/scaling-experiment.md) and an authorized validated envelope. A safety ceiling is not a concurrency target. Count total system cost, including orchestration, context duplication, escalation, retries, and review; do not assume that parallelism lowers the API bill. Only independent ready tasks may execute concurrently, with all operations admitted by the same governor.
