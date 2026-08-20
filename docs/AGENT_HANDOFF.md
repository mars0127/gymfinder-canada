# Agent Handoff and Recovery Capsule

Use this document when starting a new ChatGPT, Codex, Claude, or other AI session.

## Project summary

GymFinder Canada is a working title for a Toronto-first gym comparison website. The initial wedge is exact strength equipment, equipment manufacturers, access conditions, and selected amenities. The product presents traceable, correctable facts rather than a general review feed.

## Current status

**PLANNING**

The repository contains product foundations and the Stage 1 governance system. Production implementation is not yet authorized.

## Current operating model

- Human founders own product direction and acceptance.
- Pre-implementation planning is conducted primarily through ChatGPT and/or Codex.
- Under the current owner decision, Claude enters the default workflow when implementation is authorized.
- After implementation authorization, Codex and Claude are peer execution agents with dynamic issue-level roles.
- Independent review is risk-triggered, not automatic or model-specific.
- Figma is the visual design, prototyping, and handoff workspace.

## Accepted product constraints

- Toronto-first public scope.
- Strength-training users are the provisional first segment.
- Aim for approximately 30–50 complete profiles.
- Fact-level provenance and verification.
- `present`, `absent`, and `unknown` remain distinct.
- Structured corrections; no open reviews in MVP.
- User submissions enter moderation.
- Google Maps scraping and Reddit ingestion are prohibited.
- Gym-operator participation is optional and non-blocking.
- No payments, subscriptions, automated trials, paid ranking, or real-time crowding in MVP.
- Explainable deterministic matching before AI recommendations.
- Near-zero-cost infrastructure during MVP planning and pilot.

## Accepted planning choices

- External user interviews, surveys, and usability tests are deferred until a prototype or alpha.
- Competitor products are used as pattern evidence, not copied designs or product-data sources.
- A five-gym data calibration occurs during planning and does not block PRD or Figma work.
- Production implementation begins only after the build-ready planning package is accepted.

## Immediate planning path

1. Merge Stage 1 governance.
2. Complete the competitor UX pattern audit.
3. Draft PRD v1.
4. Create Figma information architecture, flows, design foundations, and critical screens.
5. Complete the five-gym data calibration in parallel.
6. Define data/trust and technical architecture.
7. Integrate and freeze the planning package.
8. Create the implementation backlog and planning closeout.
9. Obtain explicit founder implementation authorization.

## Source-of-truth order

1. `docs/DECISIONS.md` and accepted ADRs.
2. Accepted PRD and `docs/MVP_SCOPE.md`.
3. `docs/PROJECT_BRIEF.md`.
4. Active issue acceptance criteria.
5. Approved Figma frames for visual intent.
6. Current schema, code, migrations, and tests after implementation begins.
7. Accepted research outputs.
8. Reference documents.
9. Chat history.

## Instructions for a new AI context

Before giving consequential guidance:

- identify the current issue and stage;
- inspect relevant repository documents;
- verify current Git state when repository access is available;
- distinguish accepted decisions from suggestions;
- do not invent gym facts;
- do not silently broaden scope;
- do not treat the original discussion report as final requirements;
- do not authorize production implementation while status remains `PLANNING`.

When finishing a governed task, return:

- task/run identity when used;
- work performed;
- files or artifacts changed;
- evidence and limitations;
- failures and classification;
- scope and permission audit;
- remaining uncertainty;
- final repository or service state;
- recommended next action;
- exact final status.
