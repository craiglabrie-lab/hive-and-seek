# ADR-0005: Frontier orchestration, inexpensive workers, measured scaling

Date: 2026-10-22. Status: accepted architecture direction, authorized by the project owner. Model identities, operating settings, and production worker counts remain unselected.

## Context and decision

Use a frontier-capability model for the central Career Orchestrator and inexpensive, task-qualified models for routine specialist work. The hierarchy of responsibilities and model capabilities is the architectural choice. Select worker counts only after measuring their marginal benefit, quality, and complete system cost.

Preserve all nine logical agents and their contracts. Model tiers and executing worker instances do not change that roster. Specialist work may escalate to a frontier-capability model for a material reasoning issue while retaining its original role, evidence requirements, and independent-review boundary.

## Consequences

- Model routes need recorded capability/evaluation, privacy/tool authorization, exact versions, and prices.
- Frontier orchestration, workers, critiques, escalations, retries, and consolidation share the resource governor's root budget.
- A missing fact, user decision, or permission remains missing after escalation; no model tier can invent it.
- A serial worker baseline is an experiment reference, not a production optimum. Production capacity remains unset until qualifying measurements and operating-policy authorization exist.
- Governor ceilings remain hard limits. A validated worker target may be lower; models cannot raise ceilings or reset counters.
- Compare equal work and quality requirements. Measure API/tool cost separately from elapsed-time benefit and any explicitly valued human effort.

## Alternatives

An all-frontier configuration and a single-assistant configuration may serve as disclosed comparison baselines. A large fixed worker count without measured benefit is not selected. Lower unit pricing does not establish lower overall workflow cost.

## Scope

This decision updates the architecture, routing/reference policies, templates, and evaluation plan. It does not implement or configure a running model router, buy API access, install AI-DLC, or enable autonomous execution.

See [model hierarchy](../architecture/model-routing.md), [worker-scaling evaluation](../../evaluation/worker-scaling.md), and [ADR-0004](0004-resource-governor.md).
