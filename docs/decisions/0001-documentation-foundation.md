# ADR-0001: Documentation foundation and separate layers

Date: 2026-10-22. Status: accepted scope for this repository task.

## Context

The project owner requested folder structure, README, and non-code artifacts for Hive & Seek's ontology-driven multi-agent career system and proposed AI-DLC development approach.

## Decision

Create a documentation and planning baseline. Separate the development system that builds Hive & Seek from the career system that supports a job seeker. Do not implement or deploy the runtime in this task. Keep public artifacts generic or synthetic.

## Alternatives

- Implement a runtime immediately: outside the requested scope and premature before pilot feedback.
- Create only empty folders: insufficient to preserve the envisioned project and make the next work concrete.
- Treat AI-DLC as the career runtime: confuses development tooling with product responsibilities.

## Consequences

The repository is navigable and reviewable without claiming operational capabilities. Technology choices and detailed contracts remain proposals. A later implementation task can use this baseline without adopting an unnecessary stack now.

## Basis

Current project-owner instruction establishes the non-code scope. The two-layer distinction carries forward the design discussion. This record does not approve detailed architecture, runtime permissions, or future external actions.
