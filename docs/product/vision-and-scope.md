# Vision and scope

Status: design baseline; implementation details proposed.

## Problem

Job-search context is fragmented across resumes, listings, conversations, and interview notes. A keyword match can overlook an excellent opportunity or recommend work the person dislikes. Repeated prompting also loses the reasons behind earlier choices.

## Product intent

Help a job seeker construct a career knowledge model that captures experience, evidence, motivations, constraints, and decision rationale. Coordinate specialist roles against that shared model, challenge weak conclusions, and improve recommendations through observed outcomes and user corrections.

The user remains the authority on their preferences, professional claims, and external actions. Agents may propose extensions to the ontology, surface adjacent roles, and question inconsistent reasoning; they may not silently redefine the user's goals.

## First user journey

1. Reuse available career materials in a private workspace.
2. Identify the user's target outcome and ask focused questions about why choices matter.
3. Build an evidence register and connected ontology; resolve conflicts and review the baseline.
4. Research one role category and verify opportunity status where tools allow.
5. Explain capability, desirability, evidence quality, and tradeoffs separately.
6. Draft a truthful application artifact and submit it to independent critique.
7. Present a concrete recommendation and draft for human review.
8. Record corrections and eventual outcomes without rewriting history.

## In scope for the initial design

Decision-context model; provenance; five logical roles; shared-context handoffs; disagreement handling; one pilot workflow; application and interview support; approval boundaries; outcome and cost measures; AI-DLC adoption planning.

## Deferred

Production agent execution, scheduling, email/job-board integrations, bulk application handling, multi-user hosting, cloud deployment, knowledge-graph infrastructure, and automated learning. Resume Strategy, ATS Analysis, Interview Preparation, and Networking can become separate roles when their value is demonstrated.

## Non-goals

Guaranteed placement, ATS score guarantees, indiscriminate application volume, invented qualifications, unapproved outreach, or copying a person's hidden internal thought process. Decision records capture concise, reviewable reasons and evidence, not private model chain-of-thought.

## Success hypothesis

A versioned ontology plus independent challenge produces more useful recommendations and less re-explanation than an unstructured career chat. This remains a hypothesis until the pilot measures it against a comparable single-assistant baseline.
