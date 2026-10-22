# Planning state

Baseline date: 2026-10-22.

**Current work:** Documentation foundation only. The user has authorized repository structure, README, and non-code artifacts. Runtime implementation and AI-DLC installation are not part of this task.

| Area | State | Evidence / next action |
| --- | --- | --- |
| Product concept | Documented | Vision, requirements, roadmap |
| Decision-context ontology | Draft conceptual model | Review against a private discovery pilot |
| Agent contracts | Nine-agent baseline restored; detailed contracts remain draft | Original nine distinct agents; no grouped or deferred roles; see ADR-0003 |
| Resource governor | Authorized design addition; not implemented | Shared budget/admission specification, illustrative limits, record template, acceptance scenarios; see ADR-0004 |
| Model hierarchy and scaling | Authorized architecture direction; not implemented | Frontier orchestration, inexpensive qualified workers, bounded escalation; production worker counts unset pending measurement; see ADR-0005 |
| Career workflow | Draft | Synthetic walkthrough and blank templates |
| AI-DLC adoption | Proposed | Upstream reviewed; release/harness setup still open |
| Technology selection | Open | Record options and decisions before code |
| Private user ontology | Not created | Perform discovery outside this public repository |
| Executable runtime | Not started | Requires a later implementation task |
| Runtime evaluation | Not run | Scenarios defined; no pass claims |
| Deployment / integrations | Not configured | Deferred |

## Next bounded work

Conduct private career discovery and one guided pilot using the supplied templates. Use findings to review the proposed requirements, decision rules, and role boundaries. Then select a minimal implementation approach, if needed.

Open choices: project license, AI-DLC release/harness, provider, private storage, actual user criteria, actual governor-policy values and monetary/pricing settings, service-wide ceilings, freshness policy, and evaluation targets. Numerical throttle settings are illustrative proposals; creating a file or making a commit does not activate them or implement enforcement.

Tier-specific models/versions, qualification evidence, route policy, production worker count/envelope, and marginal-benefit thresholds also remain unselected. The checked-in routing policy is reference data, and no worker-scaling experiments have run.
