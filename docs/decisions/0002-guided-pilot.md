# ADR-0002: Guided pilot before separate executing agents

Date: 2026-10-22. Status: proposed.

## Context

The career architect concept recommends starting with a small set of roles and proving one useful workflow before adding cost and infrastructure. The broader catalogue contains nine responsibilities.

## Proposed decision

Begin with five logical roles: Orchestrator, Ontology, Market Intelligence, Fit & Application Strategy, and Critical Reasoning. Combine draft support under the fit/application role while preserving the separate contracts. Conduct one guided pilot in a private workspace.

## Alternatives and tradeoffs

| Option | Benefit | Cost / limitation |
| --- | --- | --- |
| One undifferentiated assistant | Very simple baseline | Context, critique, and responsibilities are less explicit |
| Five logical roles in one chat | Portable and easy to inspect | Simulated critique has limited independence; persistence is manual |
| Separate executing agents immediately | Tool isolation and durable task execution possible | Framework, state, budget, recovery, and integration complexity |

## Review criteria

Compare recommendation relevance, evidence accuracy, constraint handling, time, and cost against a comparable single-assistant baseline. Split roles when measured failures or context/tool boundaries justify it. No agent count guarantees quality.

## Open

Owner acceptance, pilot target category, private materials, actual criteria, sample size, and measurable targets. No runtime platform or provider is selected by this proposal.
