# Pilot scorecard

No targets or measured outcomes are asserted by this file. Set targets with the user after a comparable baseline is observed.

| Measure | Definition | Interpretation / limitation |
| --- | --- | --- |
| User-rated relevance | User's rating of each recommended opportunity with written reason | Capture sample count; preserve changes in criteria |
| Evidence coverage | Supported substantive claims / all substantive claims | Unknowns must be counted and labeled; record claim-count method |
| Unsupported claims | Number of substantive claims lacking evidence or explicit uncertainty | Fabricated career claims require correction before use |
| Constraint violations | Recommendations that contradict confirmed hard constraints | Distinguish unknown conditions from known violations |
| Re-explanation effort | User time spent restating already available context | Compare similar tasks and source availability |
| Packet effort | User minutes and total elapsed time per reviewable packet | Include correction effort and failed attempts |
| Interview conversion | Interviews obtained / applications submitted in the observed cohort | Report counts and observation window; no causal attribution to agents alone |
| Offer conversion | Offers / interviews with known outcomes | Small samples and pending outcomes limit inference |
| Token use and cost | Measured usage × dated provider prices, plus actual tool costs | Mark estimated or unavailable; do not invent usage for ordinary chat |
| Critique value | Material errors or assumptions corrected after review | More objections are not automatically better |
| Coordination efficiency | Duplicate tasks and avoidable retries per cycle | A duplicated source is not necessarily independent corroboration |
| Resource governance | Peak concurrent instances, model/tool attempts, tokens/spend consumed and reserved, review rounds, stop reasons, and incomplete checks | Count all root descendants and orchestration; distinguish estimated, reconciled, and unknown usage; manual role-play cannot claim enforced limits |
| Model hierarchy | Per-tier/model/version usage and cost, supervision, escalation, retry, and consolidation overhead | Cheap worker prices do not prove lower system cost; include failed attempts and actual route prices |
| Worker scaling | Quality-qualified cost per accepted packet, end-to-end latency/spread, and marginal benefit at each tested worker count | Hold workload/models/quality constant; production count is unselected until evidence meets declared objectives within governor ceilings |

## Comparison design

Use the same synthetic profile, listing set, evidence access, and review criteria for a basic single-assistant baseline and the proposed logical-role workflow. Record model/provider and execution mode where available. Have the user assess usefulness and factual quality, and document order effects or unequal tools. Do not imply a controlled scientific result from a single informal comparison.

## Review decision

At each pilot review, record what improved, what failed, unknowns, cost/effort, and the next bounded experiment. Preserve the nine-agent baseline; any proposed architecture change needs evidence and project-owner approval. Add infrastructure only when it addresses an observed limitation. Keep real job-search outcomes in the private [outcome tracker](../templates/outcome-tracker.csv).

Evaluate any proposed [resource-policy](../docs/architecture/resource-governor.md) adjustment using both usefulness and resource consumption. A low cost achieved by omitting required critique is not a successful optimization. Version authorized limit changes and retain consumed usage and outstanding reservations. Use the private [resource-budget record](../templates/resource-budget.md).

Use the [worker-scaling protocol](worker-scaling.md) and [experiment record](../templates/scaling-experiment.md) to compare serial and parallel execution under the [model hierarchy](../docs/architecture/model-routing.md). Report elapsed time separately from actual model/tool and other measured cost. Select capacity only from qualifying results against declared objectives; no target or savings is established by the reference policy files.
