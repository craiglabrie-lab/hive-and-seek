# Measuring the benefit of additional workers

Status: evaluation protocol only. No benchmarks have run and no production worker count has been selected.

## Question and controls

Does another concurrently executing specialist improve useful completion time, accepted output, or cost enough to justify the additional work and coordination? Keep the nine-role architecture fixed. Vary worker concurrency separately from model selection; otherwise a model change can be mistaken for a scaling benefit.

For the primary fixed-work comparison, use the same synthetic candidate/ontology version, evidence and opportunity set, task graph, required outputs, acceptance rules, context policy, model versions, routes, and resource ceilings. Count unsuccessful and unfinished work. Use a fixed-time throughput study only as a separately labeled experiment with comparable input queues and quality checks.

## Procedure

1. Define the workload class and a representative synthetic fixture. Include independent tasks and dependency-bound work. For example, requirement extraction for several supplied listings can be independent; a draft depends on the selected fit assessment.
2. Predeclare quality gates, budget/latency objectives, benefit threshold, maximum acceptable added cost, repetitions, ordering, and comparison rules. Leave a choice open if these are not selected; do not infer favorable thresholds after observing results.
3. Measure a serial baseline with one specialist executing at a time and frontier orchestration as designed. Keep the production target unset. Optionally compare an all-frontier or single-assistant configuration in a separate experiment, with model and execution differences disclosed.
4. Increase candidate concurrency in small steps only within the authorized governor and service-wide ceilings. Count active orchestration and frontier-escalated specialists correctly. Do not increase caps just to complete an experiment.
5. Repeat comparable trials. Alternate order or account for warm/cold caches and provider variability; record the actual sample size, spread, and limitations. Do not claim statistical significance from a small informal sample.
6. Validate the same required outputs and reviews for every trial. Keep failed attempts, incomplete packets, escalations, and rework in resource totals. Never compare an unreviewed candidate with a fully reviewed baseline as equivalent completed work.
7. Select the smallest tested configuration that meets the declared objectives with acceptable evidence. Reject added workers when their gain is insufficient, quality degrades, ceilings are exceeded, or overhead eliminates the benefit. Do not extrapolate to large worker counts from a small trial.
8. Record the recommended target/envelope and the actual policy authorization before production selection. Re-evaluate after material changes to models, routing, prompts, ontology, workload, or source access. Untested candidates remain unselected.

## Measures and calculations

| Measure | Calculation / interpretation |
| --- | --- |
| End-to-end elapsed time | Observed start to comparable completed packet; distinguish queue, provider, orchestration, worker, and validation time |
| API/tool cost | Sum actual metered input, output, billed reasoning, tool fees, and applicable charges using dated prices; include orchestrator, retries, critiques, escalation, and consolidation |
| Other operating cost | Report measured hosting/worker charges separately when applicable; do not invent an hourly cost simply because an agent exists |
| Cost per accepted packet | Total costs for all attempts / packets passing the same acceptance criteria; undefined if no packet passes |
| Quality | Evidence coverage, unsupported claims, hard-constraint handling, critique completion, and privacy/approval compliance |
| Coordination overhead | Measured planning, repeated context, merge/review/rework cost and time; separate observations from estimated attribution |
| Marginal latency improvement | (Baseline elapsed time minus candidate elapsed time) / baseline elapsed time, for comparable workload and positive baseline time |
| Marginal cost change | Candidate total cost minus baseline total cost; report currency and measurement basis |
| Fixed-time throughput | Accepted packets / observed interval; label separately from fixed-work cost/latency comparisons |

More workers do not imply a lower API bill. For the same work, parallelism can shorten elapsed time while token usage stays similar or rises through coordination. A lower total bill is possible only when measured changes in routing, work avoided, caching, or rework support it; attribute those differences rather than crediting worker count automatically. Keep optional monetary valuation of human time separate and explicit, with no assumed wage or productivity multiplier.

## Acceptance and selection

Fabricated professional claims, silent hard-constraint overrides, unauthorized disclosure/actions, missing required critique, or an exceeded hard ceiling disqualify a configuration. Review other quality floors and latency/cost targets before the experiment. Use measured cost and useful latency together rather than an arbitrary combined score.

A candidate qualifies only if it meets all gates and the declared objective: for example, lower total cost at required latency, or a sufficiently useful latency reduction within an explicitly accepted added-cost limit. Those thresholds remain unset until selected for an experiment. Agent agreement, self-rated confidence, or one lucky fast response is not scaling evidence.

See the [experiment template](../templates/scaling-experiment.md), [model hierarchy](../docs/architecture/model-routing.md), and [governor contract](../docs/architecture/resource-governor.md).
