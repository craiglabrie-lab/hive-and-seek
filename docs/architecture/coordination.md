# Coordination and handoff protocol

Status: proposed contract for manual and future automated execution.

## Dispatch

The orchestrator creates a task with a unique task ID, one owner, objective, required inputs, approved ontology version, allowed tools, output contract, dependencies, and effort limit. The task ledger prevents duplicate work by checking opportunity/source identity and task objective before assignment.

All roles use the [handoff template](../../templates/agent-handoff.md). Artifacts include task ID, actor, timestamps, source references, and ontology version. A manual pilot can maintain this in Markdown; no task engine currently exists.

Proposed task states: queued → running → ready-for-review → completed. A task may instead be blocked, failed, or cancelled. A blocked task names its missing input. A retry keeps the original task ID and adds an attempt number; it does not silently create a second task.

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

A bounded retry policy, concurrency limit, timeout, and token/cost budget must be chosen before autonomous execution. Parallelism is appropriate for independent evidence collection or critique, not unsynchronized writes to shared preferences or approvals.
