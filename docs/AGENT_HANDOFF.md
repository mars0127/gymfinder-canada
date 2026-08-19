# Agent Handoff Context

Use this document when starting a new ChatGPT, Codex, Claude, or other AI session.

## Project summary

GymFinder Canada is a working title for a Toronto-first gym comparison website. The initial wedge is exact strength equipment, equipment manufacturers, access conditions, and selected amenities. The product is intended to present traceable facts rather than a general review feed.

## Current stage

Discovery and pre-planning. The repository contains product and research foundations, not an approved production implementation.

## Accepted constraints

- Toronto-first public scope.
- Strength-training users are the provisional first segment.
- Aim for approximately 30–50 complete profiles.
- Fact-level provenance and verification.
- `present`, `absent`, and `unknown` remain distinct.
- Structured corrections; no open reviews in MVP.
- User submissions enter moderation.
- Google Maps scraping and Reddit ingestion are prohibited.
- Gym-operator participation is optional and non-blocking.
- No payment, subscriptions, trials, paid ranking, or real-time crowding in MVP.
- Explainable deterministic matching before AI recommendations.
- Near-zero-cost infrastructure during validation.

## Validation philosophy

No interview quota exists. Research must answer a named decision.

The immediate evidence path is:

1. founders align on decisions;
2. ten-gym source and attribute audit;
3. task-based user evidence only where uncertainty remains;
4. narrow data-model spike;
5. freeze decisions;
6. create formal project plan.

## Source-of-truth order

1. `docs/DECISIONS.md` and accepted ADRs.
2. `docs/MVP_SCOPE.md`.
3. `docs/PROJECT_BRIEF.md`.
4. Active issue acceptance criteria.
5. Research outputs.
6. Reference documents.
7. Chat history.

## Instructions for an AI session

Before giving implementation guidance:

- identify the active issue;
- read the relevant repository documents;
- state assumptions;
- distinguish accepted decisions from suggestions;
- do not invent gym data;
- do not silently broaden scope;
- do not use the attached discussion report as final requirements when it conflicts with accepted decisions.

When finishing a session, provide:

- decisions made;
- files changed;
- tests or research completed;
- unresolved questions;
- the next concrete issue.
