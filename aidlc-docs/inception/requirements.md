# Requirements baseline v0.1

Status: proposed product specification grounded in the project concept. “Must” describes intended behavior, not implemented capability. Detailed acceptance scenarios are [here](../../evaluation/acceptance-scenarios.md).

| ID | Requirement | Acceptance intent |
| --- | --- | --- |
| HS-001 | Reuse authorized career materials and conduct focused discovery | Discovery record names existing sources, target outcome, constraints, and unresolved questions |
| HS-002 | Maintain explicit entities and relationships for career and decision context | A decision connects capability, motivation/criteria, evidence, and rationale rather than storing keywords alone |
| HS-003 | Preserve provenance and epistemic status | Every substantive claim has evidence or explicit unknown status; inference is distinguishable from user confirmation |
| HS-004 | Version knowledge and retain decision history | A correction links prior/new records and identifies stale dependent outputs |
| HS-005 | Verify opportunities using actually available tools | Source, retrieval time, observed status, method, and limitations are recorded; unavailable verification is disclosed |
| HS-006 | Separate capability, desirability, and evidence strength | Fit report contains separate assessments and checks hard constraints before ranking |
| HS-007 | Generate truthful, targeted drafts | Every professional claim maps to evidence; gaps are not filled by invention |
| HS-008 | Challenge recommendations and preserve dissent | Critique identifies material assumptions or records no material issue with reasons; independence level is labeled |
| HS-009 | Coordinate the nine distinct baseline agents using shared approved context | All nine have separate contracts; each task invokes relevant agents with one owner, versioned inputs, output contract, dependencies, and duplicate-work check; no unapproved merging or deferral |
| HS-010 | Keep external actions under explicit user control | No message, submission, or private-data sharing without concrete action approval; changed payload invalidates approval |
| HS-011 | Minimize private-data access and prevent public leakage | Public examples are synthetic; private data and derived records follow approved access/retention policy |
| HS-012 | Learn from corrections and observed outcomes | Changes capture reasons; no permanent preference inferred without confirmation; outcome causality is not fabricated |
| HS-013 | Measure value, effort, and cost | Pilot records relevance, evidence quality, time, usage/cost where measurable, and observed conversion with denominators |
| HS-014 | Remain portable and honest about execution mode | Simulated roles are labeled; unavailable tools/persistence/scheduling are not claimed |
| HS-015 | Support bounded failure and session recovery in an executing runtime | Failed tasks and retries are visible; checkpoint includes snapshot and artifact versions; uncertain sends are reconciled |
| HS-016 | Separate development lifecycle from career operations | Development records and permissions cannot authorize career actions; AI-DLC is not represented as an installed career runtime |

## Quality requirements

Explain recommendations in plain language; minimize repeated questions when evidence exists; preserve source locators; isolate untrusted document instructions; keep execution bounded within the nine-agent baseline by invoking relevant agents per task. Budgets, latency, storage, retention duration, and numeric quality targets remain open until the pilot establishes a baseline.

No service level or employment outcome is guaranteed. The first implementation must pass the material truthfulness, permission, privacy, and constraint scenarios before any autonomous external action is considered.
