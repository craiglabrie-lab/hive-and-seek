# ADR-0003: Preserve the original nine-agent baseline

Date: 2026-10-22. Status: accepted correction, directed by the project owner.

Supersedes [ADR-0002](0002-guided-pilot.md).

## Context

The original career architect specification defines nine distinct career agents. The initial repository scaffold grouped several responsibilities and treated their later separation as optional. The project owner identified this mismatch and instructed that it be corrected.

## Decision

Restore these nine distinct agents as the architecture baseline:

1. Career Ontology
2. Job Market Intelligence
3. Job Fit Analysis
4. Resume Strategy
5. Recruiter & ATS Analysis
6. Interview Preparation
7. Networking
8. Critical Reasoning
9. Career Orchestrator

Keep each agent's own contract, responsibility, and handoffs. Do not combine fit assessment with resume, screening, interview, or networking duties under one replacement agent. Do not defer any of the nine agent definitions.

## Execution and scope

All nine logical roles can initially be simulated in one conversation; a separate model instance per agent is not required. The orchestrator invokes agents relevant to a task, so a packet need not use all nine. This affects task routing, not the baseline architecture.

Runtime implementation, independent agent execution, integrations, and AI-DLC installation remain outside the current documentation task. No new technology or action permissions are granted by this correction.

## Consequences

README, architecture, scope, roadmap, planning state, contracts, workflows, prompt, synthetic example, and acceptance criteria must consistently reflect nine distinct agents. Future additions, mergers, removals, or deferrals require a separate documented architecture decision approved by the project owner.
