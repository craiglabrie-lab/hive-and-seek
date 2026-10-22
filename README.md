# Hive & Seek

**Your career. Your logic. Your swarm.**

An ontology-driven multi-agent career intelligence system that learns how you make career decisions, challenges assumptions, and coordinates specialist agents to support your job search.

**Status: documentation and design foundation.** This repository contains the project structure, specifications, prompts, templates, and a synthetic walkthrough. It does not yet contain runnable software, connected services, autonomous agents, or an installed AI-DLC runtime.

## The idea

A useful career assistant needs more than a resume and a list of keywords. It needs to understand why certain work appeals to you, what your experience actually demonstrates, which constraints matter, and when your reasoning should be challenged.

Hive & Seek preserves those connections in an explicit, versioned **decision-context ontology**. Specialist roles use the same approved knowledge to research opportunities, evaluate fit, prepare truthful application materials, and learn from outcomes. Every recommendation should explain:

1. Can this person do the job?
2. Would this person want the job?
3. What evidence supports that conclusion, and what is uncertain?
4. What should happen next?

## Two layers, different jobs

| Layer | Purpose | Starting point |
| --- | --- | --- |
| Development system | Build and validate Hive & Seek through requirements, design, implementation, review, and delivery | AI-DLC adoption plan; no tooling installed |
| Career system | Help a person make and carry out evidence-backed career decisions | Guided conversation with 3–5 logical specialist roles |

[AWS Labs AI-DLC Workflows](https://github.com/awslabs/aidlc-workflows) is the proposed development workflow. It is not assumed to supply the career ontology, job-search integrations, or production agent runtime. See the [adoption plan](workflows/development/ai-dlc-adoption.md).

## Start here

- Read the [vision and scope](docs/product/vision-and-scope.md) and [requirements](aidlc-docs/inception/requirements.md).
- Explore the [architecture](docs/architecture/overview.md), [ontology](ontology/model.md), and [agent catalogue](agents/README.md).
- Try the [portable career architect prompt](prompts/hive-and-seek-career-architect.txt) in an LLM, or inspect the [synthetic pilot](examples/synthetic/pilot.md).
- Use the [templates](templates/README.md) to record evidence, reasoning, handoffs, approvals, and outcomes in a private workspace.
- Review the [roadmap](docs/product/roadmap.md), [open decisions](docs/decisions/README.md), and [acceptance scenarios](evaluation/acceptance-scenarios.md) before implementation.

## Repository map

| Folder | Contents |
| --- | --- |
| [docs/](docs/README.md) | Product definition, architecture, privacy, decisions, and glossary |
| [ontology/](ontology/README.md) | Career concepts, relationships, provenance, and decision rules |
| [agents/](agents/README.md) | Career agent contracts and development role boundaries |
| [workflows/](workflows/README.md) | Career pilot, learning loop, and development lifecycle |
| [aidlc-docs/](aidlc-docs/README.md) | Human-authored planning artifacts; not engine-generated state |
| [prompts/](prompts/README.md) | Platform-neutral discovery and design prompt |
| [templates/](templates/README.md) | Reusable blank records and registers |
| [examples/synthetic/](examples/synthetic/pilot.md) | Fictional end-to-end example |
| [evaluation/](evaluation/README.md) | Acceptance scenarios and outcome measures |
| [data/](data/README.md) | Data handling guidance; no real candidate records |
| [src/](src/README.md) | Reserved location for future application source |
| [tests/](tests/README.md) | Reserved location for future executable checks |

## First milestone

Complete one reviewable career workflow: discovery → approved ontology → verified opportunity → separate capability/desirability assessment → evidence-backed draft → independent critique → user review → outcome record. Prove this is useful before adding autonomous execution or more agents.

The initial five logical roles are Career Orchestrator, Career Ontology, Market Intelligence, Fit & Application Strategy, and Critical Reasoning. The broader catalogue documents roles that can be separated later. Logical roles in one conversation are not independently executing agents.

## Working principles

- Preserve the reasons behind decisions, including alternatives and later revisions.
- Separate facts, preferences, assumptions, inferences, and market observations.
- Ground career claims in evidence; never invent experience or results.
- Share a versioned ontology and retain dissent rather than manufacturing consensus.
- Require explicit approval for sending outreach, submitting applications, or sharing private data.
- Measure useful opportunities, conversion, accuracy, effort, and cost.

This is a public repository: commit only project documentation, blank templates, and clearly synthetic examples. Keep resumes, correspondence, personal ontology instances, credentials, and private audit records outside it. See [privacy and permissions](docs/architecture/privacy-and-permissions.md).

See [CONTRIBUTING.md](CONTRIBUTING.md) for changes and [AGENTS.md](AGENTS.md) for AI-assisted work. Licensing for this project's original materials remains an [open decision](docs/decisions/README.md).
