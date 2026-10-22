# AI-DLC adoption plan

Status: proposed development method; no installer, runtime, hooks, skills, or engine state are included in this repository.

## Why use it

The intended use of [AWS Labs AI-DLC Workflows](https://github.com/awslabs/aidlc-workflows) is to structure the work of building Hive & Seek: requirements, domain design, contracts, delivery units, implementation, evidence-based review, and operations planning. The career ontology and career agents remain product-specific work.

Upstream was reviewed on 2026-10-22 at commit [`bfb6d09d7038970f71ae21e20bc59b03f41168fc`](https://github.com/awslabs/aidlc-workflows/tree/bfb6d09d7038970f71ae21e20bc59b03f41168fc). That is a reference snapshot, not a chosen installation version. Recheck compatibility and select a release when setup is authorized.

## Lifecycle mapping

The reviewed upstream documents describe Initialization, Ideation, Inception, Construction, and Operation. Applicable stages depend on the selected workflow profile; the table below is our project mapping, not a copied engine configuration.

| Development concern | Hive & Seek planning inputs | Intended result |
| --- | --- | --- |
| Initialization | Repo structure and planning state | Real tool-generated workspace/intent state after setup |
| Ideation | Vision, intent, scope, open assumptions | Reviewed pilot objective and boundaries |
| Inception | Requirements, ontology, contracts, backlog | Reviewed units, dependencies, architecture decisions |
| Construction | Synthetic slice and acceptance scenarios | Real implementation and current verification evidence |
| Operation | Privacy, recovery, budget, outcome measures | Operable runtime only when needed and authorized |

## What to adopt or adapt

| Upstream mechanism | Proposed project use | Important limit |
| --- | --- | --- |
| Specialized development agents | Separate product, architecture, implementation, quality, and delivery work | These are not the career agents |
| Persistent project knowledge | Preserve engineering decisions and assumptions | Keep personal career data out of public development records |
| State and audit | Resume development and trace review decisions | Let real tools write their records; never fabricate approvals |
| Units and dependencies | Build a small integrated slice before expansion | Define actual contracts and executable checks first |
| Construction swarm | Later parallelize genuinely independent implementation units | Upstream has runtime, dependency, and authorization prerequisites; not automatic parallelism |
| Human gates and review evidence | Keep major choices and concrete outputs reviewable | Repository scaffolding is not adoption or a passed gate |

## Adoption sequence

1. Review guided-pilot findings and decide whether implementation is needed.
2. Select an upstream release, supported harness, model/provider, budget, and private-data boundary in an ADR.
3. Inspect the selected release's setup and licensing requirements; retain notices if anything is copied. This scaffold contains original planning prose and upstream links only.
4. Install/configure in a separately authorized setup task. Preserve this repo's instructions and planning artifacts.
5. Have the runtime generate actual state/artifact locations. Map reviewed inputs into its workflow deliberately; do not label old planning files as completed engine stages.
6. Define the smallest end-to-end slice and real verification command before broader construction. Use the selected release's own approval semantics rather than invented configuration.
7. Consider parallel construction only after dependencies, integration checks, ownership, and failure recovery are reliable.

No CLI commands, autonomous settings, or provider credentials are prescribed here because setup choices remain open.

## Reference documents

- [Upstream overview](https://github.com/awslabs/aidlc-workflows/blob/bfb6d09d7038970f71ae21e20bc59b03f41168fc/README.md)
- [Phases and stages](https://github.com/awslabs/aidlc-workflows/blob/bfb6d09d7038970f71ae21e20bc59b03f41168fc/docs/guide/04-phases-and-stages.md)
- [Construction and swarm](https://github.com/awslabs/aidlc-workflows/blob/bfb6d09d7038970f71ae21e20bc59b03f41168fc/docs/harness-engineering/08-construction-and-swarm.md)
- [State and audit](https://github.com/awslabs/aidlc-workflows/blob/bfb6d09d7038970f71ae21e20bc59b03f41168fc/docs/guide/10-state-and-audit.md)
