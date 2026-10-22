# Agent catalogue

These are logical responsibilities and prompt contracts. No agents are deployed by these files.

## Nine-agent baseline

| Agent | Responsibility | Contract |
| --- | --- | --- |
| Career Ontology | Evidence, career knowledge, decision history | [Ontology](career/ontology.md) |
| Job Market Intelligence | Opportunity research, status, employer signals | [Market intelligence](career/market-intelligence.md) |
| Job Fit Analysis | Capability, desirability, constraints, and evidence strength | [Fit analysis](career/fit-analysis.md) |
| Resume Strategy | Truthful, targeted application drafts | [Resume strategy](career/resume-strategy.md) |
| Recruiter & ATS Analysis | Screening criteria, terminology, and missing evidence | [ATS analysis](career/ats-analysis.md) |
| Interview Preparation | Role-specific practice and evidence-backed talking points | [Interview preparation](career/interview-preparation.md) |
| Networking | Contact context, outreach strategy, and drafts for approval | [Networking](career/networking.md) |
| Critical Reasoning | Independent evidence and recommendation challenge | [Critical reasoning](career/critical-reasoning.md) |
| Career Orchestrator | Dispatch, shared context, consolidation, action boundary | [Orchestrator](career/orchestrator.md) |

These nine distinct agents are the baseline for the guided pilot and future implementation. A task invokes only the relevant agents; interview preparation and networking remain defined even when a particular packet needs neither. Simulating all nine roles in one conversation does not merge their responsibilities or require nine model instances. Changes to the architecture require an explicit design decision approved by the project owner; see [ADR-0003](../docs/decisions/0003-nine-agent-baseline.md).

All roles follow the [coordination protocol](../docs/architecture/coordination.md), use [handoffs](../templates/agent-handoff.md), and respect [privacy boundaries](../docs/architecture/privacy-and-permissions.md). All personal records live privately.

The [model hierarchy](../docs/architecture/model-routing.md) assigns frontier-capability central orchestration and inexpensive, task-qualified models for routine work under the other eight contracts. A specialist may escalate a material reasoning issue without changing its role. Executing worker counts are selected only after [scaling evaluation](../evaluation/worker-scaling.md); the nine-role roster and governor ceilings do not prescribe how many workers should run.

The [development role map](development/roles.md) is separate: those roles build this product rather than perform the user's job search.
