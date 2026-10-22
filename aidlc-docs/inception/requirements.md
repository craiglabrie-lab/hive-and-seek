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
| HS-017 | Govern execution without changing the nine-agent architecture | Register executing instances; enforce the approved roster and configured root/service-wide capacity; queue excess work; governor is not an additional agent |
| HS-018 | Enforce aggregate resource admission and durable accounting | Atomically reserve shared root allowances before model/tool dispatch; count all descendants, orchestration, retries, and reviews; reconcile actual/unknown usage; block unbounded or unpriced operations |
| HS-019 | Bound loops and stop/resume safely | Enforce calls, tokens/spend, retry/review/progress/time limits; stop dispatch, drain/reconcile, checkpoint/pause; preserve counters across resumes; never bypass required critique or action approval |
| HS-020 | Reduce redundant work without dropping material context | Reuse only version/freshness/access-valid evidence; deduplicate tasks; limit context while preserving constraints and contrary evidence; report efficiency and partial-work status honestly |
| HS-021 | Use frontier central orchestration and qualified inexpensive routine workers | Resolve routes to approved model/version, task/tool/data authorization, evaluation, and prices; preserve nine roles; label unconfigured/single-model simulations honestly |
| HS-022 | Escalate specialist reasoning within the same governance boundaries | Record material reasoning issue and actual route; preserve role/critique independence and existing root/attempt/revision limits; use actual route prices; missing facts or approvals remain unresolved |
| HS-023 | Select worker concurrency only from measured benefit | Production count remains unset without qualifying workload/model-specific trials and policy authorization; compare equal work and quality, report complete cost/latency/overhead, and stay within governor ceilings |

## Quality requirements

Explain recommendations in plain language; minimize repeated questions when evidence exists; preserve source locators; isolate untrusted document instructions; keep execution bounded within the nine-agent baseline by invoking relevant agents per task. The [resource-governor contract](../../docs/architecture/resource-governor.md) defines intended enforcement. Its reference limits are illustrative; operating budgets, pricing, service-wide capacity, storage, retention, and numeric quality targets remain open until selected for a measured pilot.

No service level or employment outcome is guaranteed. The first implementation must pass the material truthfulness, permission, privacy, and constraint scenarios before any autonomous external action is considered.

The [model hierarchy](../../docs/architecture/model-routing.md) is an accepted direction. Exact providers/models, task qualifications, scaling thresholds, and production worker envelopes remain unselected; the [scaling protocol](../../evaluation/worker-scaling.md) defines how to establish evidence rather than assume an efficient worker count.
