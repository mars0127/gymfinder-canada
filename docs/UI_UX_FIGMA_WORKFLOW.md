# UI/UX and Figma Workflow

## Purpose

Figma is GymFinder's shared workspace for product structure, flows, visual design, prototyping, and frontend handoff. The workflow is designed to move quickly from competitor-pattern evidence to an implementation-ready design without making external user testing a precondition.

## Truth boundaries

| Subject | Authoritative source |
|---|---|
| Product scope and behavior | Accepted decisions and PRD |
| Visual intent and interaction presentation | Approved Figma frames and design foundations |
| Data and verification semantics | Data model, dictionary, and verification policy |
| Security and authorization | Architecture, policies, migrations, and tests |
| Running behavior | Tested production code |
| Work history and approval | GitHub issues, pull requests, and closeouts |

A Figma frame cannot authorize direct fact editing when the accepted policy requires moderation. Code cannot silently discard an approved visual or state requirement.

## Figma access

Use the founder's Figma Education access. Verify any plan- or seat-dependent capability before making it a required dependency. The MVP design process must remain possible with ordinary design files, components, variables, prototypes, and exportable context.

Both Codex and Claude may read or write Figma artifacts during implementation when configured and assigned. During planning, ChatGPT/Codex may prepare the information architecture, design briefs, content model, and Figma execution contracts.

## Recommended project and file

Create a Figma project for GymFinder and a primary file named:

```text
GymFinder — Product Design
```

Recommended pages:

```text
00 — Cover and Current Decisions
01 — Competitor Patterns
02 — Information Architecture
03 — User Flows
04 — Low-Fidelity Wireframes
05 — Design Foundations
06 — Components
07 — High-Fidelity Screens
08 — Prototype
09 — Developer Handoff
99 — Archive
```

## Page requirements

### 00 — Cover and Current Decisions

Include:

- project status;
- current MVP statement;
- Toronto-first boundary;
- provisional target user;
- links to the PRD, decision log, and relevant GitHub issues;
- latest approved design checkpoint;
- unresolved design decisions.

### 01 — Competitor Patterns

Record reconstructed patterns and annotations, not copied complete screens.

For each pattern:

- source product;
- problem addressed;
- strengths and weaknesses;
- accessibility concern;
- adopt, adapt, reject, or defer;
- GymFinder-specific rationale.

Do not reuse competitor logos, artwork, photography, marketing copy, or brand styling.

### 02 — Information Architecture

Model the MVP surfaces:

```text
Home / Search setup
Search results
Gym comparison
Gym profile
Fact evidence and freshness
Submit confirmation or correction
Submission status
Authentication
Moderation
Privacy / source / credits
```

### 03 — User Flows

Minimum flows:

1. Enter location and requirements → results.
2. Mark must-have versus preferred requirements.
3. Inspect why a gym matched, failed, or remains uncertain.
4. Compare two or three gyms.
5. Open a profile and inspect equipment, amenities, evidence, and freshness.
6. Confirm a fact.
7. Propose a correction or missing fact.
8. Sign in when contribution requires it.
9. View pending, accepted, rejected, stale, or disputed status.
10. Moderate a submission using simple internal tooling.

### 04 — Low-Fidelity Wireframes

Design mobile first, then desktop. Resolve:

- page hierarchy;
- filter grouping;
- list-first results;
- optional map placement;
- result-card information;
- comparison density;
- contribution friction;
- empty, loading, error, and zero-result states;
- unknown, stale, disputed, and unverified presentation.

Do not spend time on polished visual styling here.

### 05 — Design Foundations

Define:

- colour roles and semantic states;
- typography;
- spacing scale;
- radii and elevation;
- layout grid and breakpoints;
- focus treatment;
- icon rules;
- motion principles;
- content and status language.

Verification states must not rely on colour alone.

### 06 — Components

Initial component candidates:

- navigation;
- location input;
- search field;
- filter group;
- must-have/preferred control;
- filter chip;
- gym result card;
- match explanation;
- equipment row;
- amenity row;
- verification and freshness indicator;
- unknown-state indicator;
- comparison header and cells;
- source/evidence disclosure;
- correction form fields;
- submission status;
- buttons, inputs, dialogs, alerts, and pagination.

Create variants for relevant states rather than duplicating detached frames.

### 07 — High-Fidelity Screens

Create only after low-fidelity structure and foundations are accepted.

Minimum critical screens:

- home/search setup;
- mobile and desktop results;
- comparison;
- gym profile;
- fact evidence disclosure;
- confirmation/correction flow;
- sign-in boundary;
- pending/disputed state;
- key empty and error states.

### 08 — Prototype

Connect the critical path. The prototype demonstrates intended behavior; it does not prove production feasibility or usability.

### 09 — Developer Handoff

For each approved screen or component, provide:

- linked PRD requirement or issue;
- responsive behavior;
- states and variants;
- content rules;
- data requirements;
- unknown and error behavior;
- accessibility annotations;
- implementation notes and intentional non-goals.

## Product-specific design principles

### List first

Comparing many structured attributes is easier in a list and comparison view. A map is optional and must not be the only way to understand results.

### Must-have versus preferred

The interface should let users distinguish a disqualifying requirement from a preference. Results explain both.

### Unknown remains visible

Unknown facts must not appear as confirmed absence. The design should explain how unknown information affects matching.

### Evidence without overload

Show concise verification and freshness summaries at the decision point, with deeper source detail available on demand.

### Explainable matching

Avoid opaque scores. Show requirements met, unmet, and unknown.

### Mobile-first contribution

Confirming or correcting one fact should be a short, structured flow rather than an entire profile edit.

### Accessibility baseline

Design for:

- keyboard navigation;
- visible focus;
- semantic reading order;
- sufficient contrast;
- text resizing and reflow;
- screen-reader labels;
- non-colour status cues;
- accessible errors;
- list alternatives to spatial maps;
- motion reduction.

## Competitor inspiration rules

Use `docs/COMPETITOR_UX_PATTERN_AUDIT.md`.

A pattern may be adopted when it solves the same user problem and fits GymFinder's product and data constraints. It should be adapted when GymFinder's trust model, unknown states, or list-first comparison require a different treatment.

## Figma-to-code workflow

Before implementation:

1. Freeze the relevant requirement and Figma checkpoint.
2. Identify reusable component boundaries.
3. Define data contracts before parallel frontend/backend work.
4. Assign one primary agent per code issue.
5. Let either Codex or Claude implement according to task fit.
6. Verify responsive, state, accessibility, and acceptance behavior.
7. Record material divergence and update Figma or requirements when accepted.

Do not ask an agent to “implement the whole Figma file.” Use bounded screens, components, and flows.

## Design-ready gate

The design baseline is ready for implementation when:

- [ ] information architecture is accepted;
- [ ] critical flows are complete;
- [ ] mobile and desktop wireframes are accepted;
- [ ] design foundations exist;
- [ ] reusable components and states are defined;
- [ ] critical high-fidelity screens are accepted;
- [ ] unknown, stale, disputed, loading, empty, and error states are covered;
- [ ] accessibility annotations are present;
- [ ] handoff links requirements to frames and components;
- [ ] material open design decisions are resolved or deferred.
