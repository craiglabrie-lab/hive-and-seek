# Resource budget and governor record — TEMPLATE

Blank template. Completed real workflow records are private. This record is not executable configuration or evidence of enforced limits.

## Policy and objective

- Root workflow ID / objective:
- Policy ID / version / selected by / timestamp:
- Mode: advisory manual exercise / governed runtime
- Approved nine-agent roster reference:
- Deployment/service-wide ceilings, if applicable:
- Ontology snapshot and evidence/input versions:
- Model/provider and price version/date:
- Monetary cap, currency, included tool fees:
- Limits: concurrent workers; model/tool attempts; aggregate input/output/billed-reasoning tokens; per-call input/output; retries; review rounds; no-progress rounds; call/task/workflow time:
- Task allowances and required review/validation work reserved or planned:
- Metering unavailable / unresolved settings / activation blocked reason:

## Ledger summary

| Measure | Limit | Consumed | Outstanding reservation | Remaining available | Evidence / uncertainty |
| --- | --- | --- | --- | --- | --- |
| Concurrent workers | | | | | |
| Model-call attempts | | | | | |
| Tool-call attempts | | | | | |
| Model tokens | | | | | |
| Monetary spend | | | | | |
| Workflow execution time | | | | | |

Reconcile different units separately. Count all descendant work and orchestrator calls. Do not record unknown usage as zero. Preserve operation-level receipts privately; do not place candidate information in public telemetry.

## Admission and stop events

| Timestamp | Task / operation ID | Role | Admit / queue / block / stop / reconcile | Reason | Reservation or actual usage | Result reference |
| --- | --- | --- | --- | --- | --- | --- |
| | | | | | | |

- Peak active workers:
- Retries and artifact review/revision rounds:
- Material progress / no-progress count:
- Duplicate work avoided and freshness/permission basis for reuse:
- Governor stop reason and workflow state:

## Checkpoint and resume

- Completed artifacts and versions:
- Required review/approval still incomplete:
- Queued, failed, cancelled, and unfinished tasks:
- In-flight operations and unresolved reservations:
- External action results requiring reconciliation:
- Accumulated elapsed time and original task deadlines:
- Proposed next step:
- Actual user-authorized adjustment, instruction reference, timestamp, old/new limits, and new policy version, if any:
- Resumption record showing retained counters, reservations, and input-version revalidation:
