# Build-Ready Planning Roadmap

## Current status

**Project status: `PLANNING`**

The objective is to produce a coherent, build-ready plan without making external user interviews, gym-operator contact, or broad market research prerequisites.

## Stage 1 — Governance and workspace alignment

**Status: complete when the Stage 1 governance patch is merged.**

Outputs:

- shared agent policy;
- peer Codex/Claude implementation model;
- ChatGPT/Codex planning control layer;
- risk-triggered review policy;
- Figma design workflow;
- revised decisions and ADRs;
- planning templates and backlog;
- explicit deferral of external user testing;
- five-gym calibration instead of a ten-gym audit gate.

No production application code belongs in Stage 1.

## Stage 2 — Competitor UX pattern audit

Study direct and adjacent products to identify useful patterns for:

- landing and location entry;
- filter organization;
- must-have versus preferred requirements;
- list and map behavior;
- result-card hierarchy;
- comparison;
- gym-profile structure;
- equipment presentation;
- verification, freshness, and unknown states;
- contribution and correction flows;
- account timing;
- mobile and accessibility behavior.

For every observed pattern, record:

- source product and retrieval date;
- the user problem it addresses;
- strengths and weaknesses;
- `adopt`, `adapt`, `reject`, or `defer`;
- GymFinder-specific reasoning.

**Output:** `docs/COMPETITOR_UX_PATTERN_AUDIT.md` completed with supporting research notes and a corresponding Figma pattern page.

## Stage 3 — Product Requirements Document

Create the PRD using accepted decisions, founder direction, competitor patterns, source policy, and verification policy.

The PRD must define:

- problem and target user;
- jobs and core use cases;
- functional requirements;
- must-have and preferred matching behavior;
- treatment of unknown facts;
- results, comparison, and profile requirements;
- correction and moderation flow;
- account timing;
- non-goals;
- pilot success, pause, and revision criteria;
- assumptions not yet validated by live usage.

**Output:** accepted PRD v1.

## Stage 4 — Figma information architecture and product design

Use `docs/UI_UX_FIGMA_WORKFLOW.md`.

Create:

1. file cover and current decisions;
2. competitor-pattern page;
3. information architecture;
4. critical user flows;
5. low-fidelity mobile and desktop wireframes;
6. design foundations;
7. initial reusable components;
8. high-fidelity critical screens;
9. clickable critical-path prototype;
10. developer-handoff annotations.

Critical paths:

- enter location and requirements;
- view explainable results;
- compare gyms;
- view a gym profile and fact evidence;
- submit a structured confirmation or correction;
- view pending or disputed states.

**Output:** accepted Figma design baseline.

## Stage 5 — Five-gym data calibration, in parallel

Select five varied Toronto facilities and attempt to resolve the candidate P0 fields without operator contact.

Record for each fact:

- value;
- present, absent, or unknown;
- source and date;
- confidence;
- contradictions;
- maintenance difficulty.

The calibration should answer:

- which identity source is most usable;
- which fields are realistically obtainable;
- which fields should be required, optional, or removed;
- how source records and canonical gyms should be separated;
- what completeness threshold is credible;
- how frequently facts may need review.

**Output:** five records plus a data-feasibility synthesis. Expand only if the first five are insufficiently varied.

## Stage 6 — Data, trust, and technical architecture

### Data and trust

Define:

- canonical gym identity;
- source records and licensing metadata;
- equipment taxonomy;
- gym facts and fact states;
- evidence and observation dates;
- freshness;
- corrections, disputes, and moderation history;
- user and future staff relationships;
- completeness calculations.

### Technical architecture

Define:

- framework and repository structure;
- Supabase boundaries and alternatives;
- server/client responsibilities;
- authentication timing;
- deterministic matching and query flow;
- storage and evidence-photo policy;
- caching, mapping, deployment, and near-zero-cost limits;
- security, privacy, accessibility, observability, and backups;
- test strategy.

Use a bounded spike only when documentation and small fixtures cannot resolve a material question.

**Output:** accepted data model, architecture, security baseline, and test strategy.

## Stage 7 — Planning integration and freeze

Reconcile the PRD, Figma, source policy, verification policy, schema, and technical architecture.

Resolve contradictions such as:

- Figma allowing direct edits while policy requires moderation;
- UI treating unknown as absent;
- comparison screens requiring fields the schema cannot support;
- PRD requiring data the five-gym calibration could not obtain;
- client-side behavior that bypasses server or RLS enforcement.

Resolve or explicitly defer every open decision that affects implementation.

**Output:** frozen build-ready planning package.

## Stage 8 — Implementation backlog and planning closeout

Create dependency-ordered epics and issues for:

1. repository and application foundation;
2. canonical gym and fact model;
3. seed data and administration;
4. deterministic search and matching;
5. results and comparison;
6. gym profile;
7. authentication;
8. structured corrections;
9. moderation;
10. verification and freshness;
11. accessibility and responsive design;
12. deployment and pilot readiness.

Each issue must include an owner, primary agent, mode, branch, dependencies, acceptance evidence, permissions, and review trigger.

Create a planning closeout/recovery capsule before authorizing production implementation.

## Build-ready gate

Implementation may be authorized when:

- [ ] Stage 1 governance is merged.
- [ ] Competitor-pattern audit is complete.
- [ ] PRD v1 is accepted.
- [ ] Figma information architecture, critical flows, and design baseline are accepted.
- [ ] Five-gym calibration has informed P0 fields and source strategy.
- [ ] Data model and equipment taxonomy are accepted.
- [ ] Technical architecture and security/privacy baseline are accepted.
- [ ] Verification and moderation rules align across requirements, Figma, and schema.
- [ ] Implementation backlog is dependency ordered.
- [ ] Pilot measurement and pause criteria are defined.
- [ ] Open implementation-affecting decisions are accepted or deferred.

## Explicitly unnecessary before implementation planning is complete

- external user interviews or surveys;
- usability testing;
- gym partnerships or operator contact;
- trial-code commitments;
- payment validation;
- a final name, logo, or domain;
- 30–50 completed profiles;
- Canada-wide research;
- production deployment.
