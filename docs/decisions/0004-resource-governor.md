# ADR-0004: Add an execution resource governor

Date: 2026-10-22. Status: accepted design addition, authorized by the project owner. Numerical policy values remain illustrative proposals.

## Context

The coordination design already calls for bounded retries, concurrency, timeouts, and token/cost budgets. These need a concrete enforcement contract so the career workflow cannot create excessive instances, duplicate tasks, repeated critique loops, or uncontrolled aggregate spending.

## Decision

Specify a resource governor as part of the future orchestration software. Every executing instance, model call, and tool operation must use admission checks and a shared root-workflow ledger. Descendants, retries, critique, and orchestration share the same allowance. Reservations, actual usage, uncertainty, deadlines, and stop reasons survive recovery.

Keep all nine career agents and their responsibilities. The governor is not another agent, does not remove roles, and does not grant permissions for career actions. It enforces policy outside the LLM's discretionary instructions.

## Alternatives and consequences

- Prompt-only economy instructions cannot provide hard execution bounds.
- Per-agent budgets alone can leave aggregate cost and concurrency unbounded.
- A concurrency cap alone does not bound sequential model calls or repeated review.

The selected design combines capacity, call, token, monetary, retry, review, progress, and time limits. On exhaustion, preserve completed work and unresolved operations, then pause with required checks marked incomplete. Numerical values need review against measured pilot behavior; agents cannot raise limits themselves.

## Scope

This change adds [the specification](../architecture/resource-governor.md), a [reference policy](../../examples/synthetic/resource-policy.json), a [record template](../../templates/resource-budget.md), and acceptance coverage. It does not install a runtime, enable autonomous execution, or claim the throttle is implemented. Monetary settings are intentionally unset until an actual operating budget and pricing basis are selected.
