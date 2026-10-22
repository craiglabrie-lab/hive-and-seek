# Career and decision-context model v0.1

Status: proposed conceptual specification. IDs below describe record conventions, not implemented schemas.

## Entities

| Concept | Suggested ID | Core attributes |
| --- | --- | --- |
| Person / professional identity | PERSON-001 | Narrative, desired identity, verification state |
| Experience | EXP-001 | Organization, role, dates, responsibilities, project, scope |
| Capability | CAP-001 | Skill or behavior, proficiency description, recency, evidence |
| Accomplishment | ACC-001 | Action, context, outcome, metric, evidence |
| Motivation | MOT-001 | Energizing work, disliked work, stated reason |
| Preference | PREF-001 | Desired condition, importance, rationale, confirmation |
| Constraint / exclusion | CON-001 | Condition, hard/soft classification, scope, reason, exceptions |
| Target role / organization | TARGET-001 | Category, industry, organization, reason for interest |
| Opportunity | OPP-001 | Source identity, title, employer, location, requirements, observed status |
| Requirement | REQ-JOB-001 | Exact or paraphrased requirement, source locator, required/preferred/unclear |
| Evidence | EVID-001 | Claim, source, locator, dates, verification, confidence, limitations |
| Decision | DEC-001 | Choice, context, reasons, alternatives, assumptions, tradeoffs, outcome |
| Market signal | SIGNAL-001 | Observation, sample/source scope, observed date, uncertainty |
| Search event / outcome | EVENT-001 | Application/interview/feedback stage, date, evidence, observed outcome |

These concepts cover professional identity, experience, capabilities, motivations, opportunity criteria, exclusions, decision rationale, evidence, market signals, and search history.

## Relationships

| Relation | From → to | Interpretation |
| --- | --- | --- |
| demonstrates | Accomplishment → Capability | An observed result supports a capability claim |
| supported_by | Claim or Decision → Evidence | The source supports this precise assertion |
| motivates | Motivation → Preference | Explains why a preference matters |
| constrains | Constraint → Opportunity or Target | Limits acceptable options |
| requires | Opportunity → Requirement | Connects a listing to its stated criteria |
| matched_by | Requirement → Capability | Indicates relevant evidence; not proof of full qualification |
| conflicts_with | Claim or Criterion → Claim or Criterion | Preserves unresolved inconsistency |
| challenges | Critique/Decision → Claim/Decision | Links counterevidence or alternative interpretation |
| informed_by | Decision → Preference, Constraint, Signal | Makes evaluation criteria traceable |
| resulted_in | Decision → Search event | Links choice to observed outcome without implying causation |
| supersedes | New record → Prior record | Revises a judgment while preserving history |

Relations need their own source, author, and epistemic status when inferred. A verified accomplishment does not automatically verify an agent's interpretation of it.

## Common metadata

Each substantive record carries: ID; record version; ontology snapshot version; created/updated timestamps with timezone; author or agent; epistemic type (fact, stated preference, hypothesis, inference, observation); verification state (unverified, user-confirmed, source-verified, disputed); confidence label and reason; source/evidence IDs; sensitivity; and optional supersedes link.

User confirmation verifies what the person states; it is not independent verification of every historical assertion. Unknown dates, compensation, and proficiency remain unknown. A confidence label is qualitative, not a probability of truth.

## Decision record requirements

Capture the decision question, context, selected option, why, alternatives considered, assumptions and gaps, supporting and conflicting evidence, relevant constraints, tradeoffs, actor, date, confidence, outcome, and reason for any revision. Link consequential downstream artifacts so a changed preference can invalidate stale advice.

## Example reasoning path

Synthetic accomplishment ACC-001 demonstrates capability CAP-001. Evidence EVID-001 supports the accomplishment. Motivation MOT-001 explains preference PREF-001 for mentoring. Opportunity OPP-001 includes mentoring responsibilities. A fit decision links all five records and explicitly marks the inference that mentoring scope improves desirability.

## Versioning and corrections

Use a snapshot label such as career-v1, incremented after reviewed changes. Agents propose updates; the ontology role consolidates them. The user confirms changed preferences, hard constraints, and disputed personal facts. Preserve the previous snapshot or a change history, including revision reasons. Retire or invalidate dependent outputs when their inputs change. Never learn a permanent preference from one rejected recommendation without confirmation.
