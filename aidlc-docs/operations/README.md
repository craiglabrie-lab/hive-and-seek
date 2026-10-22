# Operations planning

No application is deployed. Before a persistent runtime is operated, define:

- Private storage, access, backup, export, retention, and deletion.
- Task checkpoints, error visibility, bounded retries, and duplicate-action reconciliation.
- Selected [resource-governor policy](../../docs/architecture/resource-governor.md), monetary budget/pricing, deployment-wide ceilings, and per-root concurrency/call/token/time/retry/review/progress limits. The checked-in example is not active configuration.
- Durable atomic budget reservations, metering reconciliation, in-flight cancellation, and paused-run recovery without resetting counters. Unknown operation results remain reserved until reconciled.
- Source freshness policy and handling of unavailable or revoked integrations.
- Approval records tied to concrete actions and payload versions.
- Logging that supports diagnosis without exposing private records.
- Change review, rollback, incident response, and evaluation regressions.

Operating targets remain open until a working slice and measurable baseline exist. Complete a private [resource-budget record](../../templates/resource-budget.md) for each governed run and verify HS-017 through HS-020 before claiming throttle enforcement. Do not add fictitious dashboards, uptime claims, or operational success records.
