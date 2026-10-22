# Operations planning

No application is deployed. Before a persistent runtime is operated, define:

- Private storage, access, backup, export, retention, and deletion.
- Task checkpoints, error visibility, bounded retries, and duplicate-action reconciliation.
- Per-run token/cost limits, concurrency, timeouts, and cost reporting.
- Source freshness policy and handling of unavailable or revoked integrations.
- Approval records tied to concrete actions and payload versions.
- Logging that supports diagnosis without exposing private records.
- Change review, rollback, incident response, and evaluation regressions.

Operating targets remain open until a working slice and measurable baseline exist. Do not add fictitious dashboards, uptime claims, or operational success records.
