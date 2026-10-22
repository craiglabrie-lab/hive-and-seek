# Synthetic pilot: Avery's career decision

**All people, organizations, roles, evidence, figures, and outcomes below are fictional. This is an illustrative walkthrough, not a live posting, executed agent run, or evaluation result.**

## 1. Discovery and evidence

Avery wants a customer education role with meaningful mentoring. Avery enjoys helping colleagues explain complex products but does not want frequent travel. No actual resume or external account is used.

| Evidence ID | Fictional claim | Source locator | Epistemic / verification status |
| --- | --- | --- | --- |
| EVID-001 | Avery designed six onboarding workshops and coached two facilitators | Synthetic source brief, paragraph 1 | Fictional fixture fact |
| EVID-002 | Avery enjoys developing other facilitators | Synthetic discovery answer, paragraph 2 | Fictional stated preference |
| EVID-003 | Travel above one day per month is unacceptable | Synthetic discovery answer, paragraph 3 | Fictional confirmed hard constraint |
| EVID-004 | The fictional Clearpath Learning role includes facilitator coaching and occasional travel; frequency unstated | Synthetic posting brief, paragraph 4 | Fictional fixture observation; no live verification |

## 2. Ontology snapshot career-demo-v1

| Record | Meaning | Relationships |
| --- | --- | --- |
| ACC-001 | Designed onboarding workshops and coached facilitators | supported_by EVID-001; demonstrates CAP-001 |
| CAP-001 | Workshop design and facilitator coaching | supported_by EVID-001 |
| MOT-001 | Enjoys helping facilitators develop | supported_by EVID-002; motivates PREF-001 |
| PREF-001 | Wants mentoring responsibilities | informed by MOT-001 |
| CON-001 | At most one travel day per month | supported_by EVID-003; constrains OPP-001 |
| OPP-001 | Clearpath Learning customer education role | supported_by EVID-004; travel frequency unknown |

The capability relation is an interpretation grounded in the accomplishment. It does not establish expertise with unstated tools or programs.

## 3. Task ownership and handoff

The Career Orchestrator assigns distinct illustrative tasks using career-demo-v1:

| Agent | Task in this example |
| --- | --- |
| Career Ontology | Maintain the synthetic snapshot and evidence relationships |
| Job Market Intelligence | Supply EVID-004 as a synthetic listing without claiming current hiring status |
| Job Fit Analysis | TASK-DEMO-001: assess capability, desirability, and the travel constraint |
| Resume Strategy | TASK-DEMO-002: prepare the evidence-backed draft paragraph |
| Recruiter & ATS Analysis | TASK-DEMO-003: check the draft against known listing criteria without adding unsupported keywords |
| Interview Preparation | Defined in the baseline; no interview-preparation task needed for this packet |
| Networking | TASK-DEMO-004: draft the travel-clarification question for review; do not send |
| Critical Reasoning | TASK-DEMO-005: challenge the assessment, draft, and unresolved assumptions |
| Career Orchestrator | Route handoffs and assemble the final review packet |

Each role retains its own contract. An agent without a task in this packet remains part of the nine-agent architecture.

Expected outputs: fit assessment, truthful draft paragraph, critique, and consolidated decision. Execution mode: illustrative roles only. No agents actually ran and no token or cost measurements were collected.

## 4. Fit assessment

| Dimension | Assessment | Reason |
| --- | --- | --- |
| Hard constraints | Needs clarification | “Occasional travel” does not establish compliance with CON-001 |
| Capability | Supported for workshop design and coaching | ACC-001 and CAP-001 provide relevant evidence; other requirements remain unknown |
| Desirability | Promising | Stated mentoring duties align with MOT-001 and PREF-001 |
| Evidence strength | Limited by travel ambiguity and synthetic source | No claim about a real employer, posting, salary, or hiring status |

Proposed recommendation: **clarify**, rather than proceed unconditionally. A capability match cannot resolve the travel unknown.

## 5. Draft and claim mapping

Illustrative private draft version DRAFT-DEMO-v1:

> I have designed six onboarding workshops and coached two facilitators. I am interested in a role where I can combine workshop design with developing other facilitators.

The first sentence maps to EVID-001. The second maps to EVID-002 and PREF-001. No claim of platform expertise or quantified business impact is added.

## 6. Critique and disposition

Illustrative objection: matching mentoring interests is useful, but travel is a hard constraint and other role requirements have not been evaluated. The limited source cannot support an overall “strong fit” conclusion.

Disposition: retain the promising mentoring signal, narrow the capability claim, mark the assessment partial, and recommend clarification. This text demonstrates critique structure; it does not assert that an independently executing critic performed a review.

## 7. Decision record

| Field | Illustrative value |
| --- | --- |
| Decision ID | DEC-DEMO-001 |
| Snapshot | career-demo-v1 |
| Question | Should Avery pursue OPP-001? |
| Proposed choice | Clarify travel and remaining requirements first |
| Why | Relevant capability and motivation are supported; the hard-constraint result is unknown |
| Alternative | Decline immediately; rejected provisionally because ambiguity is not proof of a violation |
| Assumption | Employer may be able to state travel expectations; unverified |
| Next action | Prepare a travel-clarification question for user review |
| Approval state | No real user approval; no message sent |
| Observed outcome | None; fictional design example only |

## 8. Revision example

Suppose a later synthetic source says the role requires four travel days per month. Append EVID-005 and a new opportunity version. Create career-demo-v2 and DEC-DEMO-002 superseding DEC-DEMO-001. Recommend decline under CON-001 unless the user explicitly changes or waives that constraint. Mark earlier advice stale and record why the recommendation changed. Do not erase the original context or infer a new travel preference.
