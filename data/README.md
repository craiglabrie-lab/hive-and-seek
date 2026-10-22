# Data boundary

No real career data is stored here. Real candidate material and its derivatives must remain in a separately controlled private location.

The ignore rules exclude `/private/`, `/data/private/`, `/data/raw/`, `/data/exports/`, `/data/embeddings/`, `/runtime/`, and `/logs/` to reduce accidental commits. These exclusions are not a storage architecture or security control. Prefer a private workspace outside this checkout, especially when using public repository tools.

Use [blank templates](../templates/README.md) as a starting point and [synthetic examples](../examples/synthetic/pilot.md) for shared design work. Do not copy a real person's history here and merely change the name.

Private source records, ontology snapshots, claims, derived drafts, approvals, and outcomes need consistent access, retention, export, and deletion rules before production use. See [privacy and permissions](../docs/architecture/privacy-and-permissions.md).
