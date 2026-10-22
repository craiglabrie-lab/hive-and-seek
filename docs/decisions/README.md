# Decision index

Keep product architecture decisions here. Individual career choices belong in private decision records using the [template](../../templates/decision-record.md).

| ID | Decision | Status |
| --- | --- | --- |
| ADR-0001 | Establish a documentation foundation and separate development from career operations | Accepted scope for the current task |
| ADR-0002 | Earlier proposal to consolidate roles for a guided pilot | Superseded by ADR-0003; not accepted |
| ADR-0003 | Preserve the original nine distinct career agents | Accepted correction |
| ADR-0004 | Add a shared resource governor for bounded execution | Accepted design addition; numerical policy values illustrative |
| ADR-0005 | Frontier orchestration, inexpensive workers, and measured worker scaling | Accepted architecture direction; models and production counts unselected |

- [ADR-0001](0001-documentation-foundation.md)
- [ADR-0002](0002-guided-pilot.md)
- [ADR-0003](0003-nine-agent-baseline.md)
- [ADR-0004](0004-resource-governor.md)
- [ADR-0005](0005-model-hierarchy-and-measured-scaling.md)

## Open choices

Project license; AI-DLC release/harness; model/provider; persistent runtime/framework; ontology encoding; private storage; access/retention/export/deletion; user-specific criteria and weights; source freshness policy; actual resource-policy values and monetary/pricing settings; service-wide ceilings; evaluation sample and success thresholds. The governor's architecture is specified in ADR-0004; the example numerical policy is not an approved operating budget.

ADR-0005 establishes the model hierarchy and measurement-first scaling direction. Exact tier models, routing evaluations, production worker counts/envelopes, and benefit/tradeoff thresholds remain open. A governor ceiling must not be treated as an empirically selected worker count.

An open item is not a blocker to this authorized documentation scaffold. Resolve the relevant items before implementing the feature that depends on them. Do not select a legal license on the owner's behalf merely because the repository is public.

Statuses: proposed, accepted, rejected, superseded. Supersede by linking a new record; preserve the old rationale. Record who actually accepted a choice and when. A generated artifact does not establish approval.
