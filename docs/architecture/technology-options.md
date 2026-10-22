# Technology options

Status: open; this table compares design options rather than selecting products.

| Concern | Simplest pilot | Possible later option | Decision trigger |
| --- | --- | --- | --- |
| Role execution | One LLM conversation with explicit roles | API orchestration or agent framework | Need for durable, separately executing tasks |
| Knowledge storage | Versioned private Markdown and CSV records | Structured database; graph representation if needed | Proven retrieval, relationship, or concurrency limitations |
| Ontology representation | Human-readable entity and relation model | JSON Schema, RDF/OWL, or graph schema | Interoperability or validation requirement |
| Market research | User-supplied listing or authorized browsing | Approved job-data integration | Demonstrated freshness/volume need and access rights |
| Persistence | Manual snapshot and session summary | Durable checkpoints and task queue | Lost progress or recovery burden in pilot |
| Evaluation | Manual labeled scenarios | Automated fixtures and regression checks | Executable workflow exists |
| Hosting | None required | Local service or managed hosting | Actual multi-session or multi-user requirement |
| Development method | Documentation-led planning | Pinned AI-DLC release and selected harness | Implementation is authorized and setup choices made |

Choose using maintainability, evidence quality, privacy, portability, recovery, and measured cost. A graph database, vector search, cloud platform, and nine separate model instances are not prerequisites for an ontology-driven pilot.

Before committing to an executing runtime, record the model/provider, harness, allowed tools, private storage, recurring budget, retry/concurrency limits, and deletion policy in decision records. Compare at least one simple alternative. Do not add install instructions until the selected versions and workflow have been verified.
