# Agent catalogue

These are logical responsibilities and prompt contracts. No agents are deployed by these files.

## Proposed five-role pilot

| Pilot role | Logical responsibilities | Contract |
| --- | --- | --- |
| Career Orchestrator | Dispatch, shared context, consolidation, action boundary | [Orchestrator](career/orchestrator.md) |
| Career Ontology | Evidence, career knowledge, decision history | [Ontology](career/ontology.md) |
| Job Market Intelligence | Opportunity research, status, employer signals | [Market intelligence](career/market-intelligence.md) |
| Fit & Application Strategy | Fit plus resume, screening, interview, and outreach drafts as needed | [Fit](career/fit-analysis.md), [resume](career/resume-strategy.md), [ATS](career/ats-analysis.md), [interview](career/interview-preparation.md), [networking](career/networking.md) |
| Critical Reasoning | Independent evidence and recommendation challenge | [Critical reasoning](career/critical-reasoning.md) |

The nine contracts preserve the broader design without requiring nine model instances. Split responsibilities only after the pilot shows a need. Combining fit and drafting must not remove independent critique.

All roles follow the [coordination protocol](../docs/architecture/coordination.md), use [handoffs](../templates/agent-handoff.md), and respect [privacy boundaries](../docs/architecture/privacy-and-permissions.md). All personal records live privately.

The [development role map](development/roles.md) is separate: those roles build this product rather than perform the user's job search.
