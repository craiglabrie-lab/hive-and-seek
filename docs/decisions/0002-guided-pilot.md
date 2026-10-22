# ADR-0002: Earlier guided-pilot consolidation proposal

Date: 2026-10-22. Status: superseded by [ADR-0003](0003-nine-agent-baseline.md). This proposal was not accepted and does not govern the architecture.

## Context

The initial documentation scaffold proposed consolidating the original nine career agents for a guided pilot. This was an assistant-authored design change, not an agreed project decision.

## Disposition

The project owner requested restoration of the original nine-agent specification. ADR-0003 replaces the consolidation proposal with nine distinct agents throughout the README, contracts, workflows, prompt, and evaluation criteria.

## Retained principle

Begin with a bounded, reviewable workflow before adding runtime infrastructure. All nine roles may be simulated in one conversation with separate responsibilities and handoffs. Choosing relevant agents for a task does not change the architecture.

This historical record preserves the reason for the correction. No runtime platform, provider, installation, or external-action permission is selected here.
