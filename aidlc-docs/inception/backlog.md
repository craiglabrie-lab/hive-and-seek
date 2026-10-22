# Initial backlog and proposed work units

Status: planning only. No issue assignments, estimates, or delivery promises.

| Story | As a job seeker, I want… | Requirements | Proposed unit |
| --- | --- | --- | --- |
| US-01 | My existing career material reused with questions only for gaps | HS-001, HS-003 | U1 Context and evidence |
| US-02 | The system to remember why criteria matter and what changed | HS-002, HS-004 | U1 Context and evidence |
| US-03 | Current opportunity facts with uncertainty made visible | HS-005 | U2 Opportunity intake |
| US-04 | To distinguish jobs I can do from jobs I would enjoy | HS-006 | U3 Fit assessment |
| US-05 | Targeted application drafts I can defend as true | HS-007 | U4 Draft and critique |
| US-06 | A challenge to weak recommendations and assumptions | HS-008 | U4 Draft and critique |
| US-07 | One coherent result without duplicated work | HS-009, HS-014 | U5 Coordination and recovery |
| US-08 | Control over private data and every external action | HS-010, HS-011 | Cross-cutting boundary |
| US-09 | Corrections and outcomes to improve later advice | HS-012, HS-013 | U6 Learning and measures |
| US-10 | To resume failed or interrupted work without false completion | HS-015 | U5 Coordination and recovery |

## First integrated slice

Use one synthetic profile, a supplied synthetic listing, one ontology version, a fit report, a draft paragraph, critique, and a review packet. No external integration is required. Implementing this slice is deferred; the current walkthrough is a design example, not a working skeleton.

## Dependency order

U1 precedes U2/U3; U2 supplies facts to U3; U3 precedes U4; U5 integrates these contracts; U6 consumes review/outcome records. Privacy, permission boundaries, and evidence checks apply from the first unit. Refine these units into an executable dependency plan after technology selection; do not treat this prose as an engine DAG.

## Before code

Review the guided pilot; select representation, storage, and execution mode; set an evaluation baseline and budget; choose whether to adopt AI-DLC; define actual executable acceptance checks. Keep optional integrations out until a user need justifies them.
