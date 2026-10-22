# Guided career pilot

Status: proposed procedure. Perform real-person work in a private workspace; only synthetic examples belong in this repository.

| Step | Work and output | Review boundary |
| --- | --- | --- |
| 1 Discovery | Reuse authorized materials; identify objective, criteria, reasons, and gaps using the discovery template | Confirm unresolved personal facts and priorities |
| 2 Knowledge baseline | Create evidence register, relationships, decision rules, and career-v1 snapshot | User reviews the ontology and constraints |
| 3 Architecture | Preserve all nine distinct agents and define task IDs, relevant-agent assignments, inputs, permitted tools, and output contracts | Explicitly label simulated roles; do not merge responsibilities |
| 4 Opportunity intake | Take one supplied posting or research within one role category; deduplicate and record freshness | Missing status or requirements remain unknown |
| 5 Assessment | Check constraints; map requirements to evidence; explain capability and desirability separately | Show uncertainty and strongest mismatch |
| 6 Draft | Resume Strategy prepares one targeted application artifact; Recruiter & ATS Analysis reviews screening alignment and sends recommendations back to Resume Strategy | Unsupported claims are omitted or flagged |
| 7 Challenge | Critic forms an initial evidence-based view, then inspects recommendation and draft | Record objections, corrections, and remaining dissent |
| 8 Consolidation | Present fit report, draft, sources, critique, and next action | User can revise, accept the draft, or decline |
| 9 Action | Pilot ends at a reviewable packet; user may act manually | A future tool action requires its own explicit approval |
| 10 Learn | Record outcome, correction, time/cost, and next experiment | Do not infer outcomes or silently change preferences |

Use the [templates](../../templates/README.md). The [synthetic walkthrough](../../examples/synthetic/pilot.md) shows artifact relationships without a real account or live posting.

Career Orchestrator coordinates tasks, Career Ontology maintains shared knowledge, Job Market Intelligence supplies opportunity evidence, and Job Fit Analysis assesses suitability. Resume Strategy, Recruiter & ATS Analysis, and Critical Reasoning retain separate draft, screening, and challenge responsibilities. Interview Preparation and Networking are part of the same baseline and receive their own tasks when interview coaching or outreach preparation is needed. An agent need not run in every packet to remain included in the architecture.

For executing-agent pilots, apply the [model hierarchy](../../docs/architecture/model-routing.md): frontier central orchestration, qualified inexpensive routine workers, and bounded specialist escalation. Choose production worker counts only from [qualifying measurements](../../evaluation/worker-scaling.md), with all routes/calls admitted by the resource governor. A guided single-model exercise is labeled simulation of these responsibilities and does not establish tiered execution, enforced usage limits, or scaling gains.

Completion means one coherent packet exists with traceable claims, visible gaps, critique, and a decision record. A submitted application or interview is not required to complete a draft-only pilot; longer-term outcomes are recorded when observed.
