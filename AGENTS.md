# AGENTS.md — GymFinder Project-Agent Instructions

These instructions apply to ChatGPT, Codex, Claude Code, and any future AI agent working from this repository.

## Authority model

- The human founders own product direction, scope, acceptable risk, and final approval.
- During the current **PLANNING** stage, ChatGPT and/or Codex act as the supervising research, product, architecture, and continuity layer. Under the current owner decision, Claude enters when implementation is authorized.
- After implementation is explicitly authorized, Codex and Claude are peer execution agents. Either may research, design, implement, test, debug, document, or review.
- Agent roles are assigned per issue. No model has a permanent implementation or review monopoly.
- Important changes require human approval before merge or release.

## Source-of-truth order

When sources conflict, use this order:

1. Accepted decisions and ADRs in `docs/DECISIONS.md` and `docs/decisions/`.
2. The accepted PRD and `docs/MVP_SCOPE.md` once the PRD exists.
3. `docs/PROJECT_BRIEF.md`.
4. The active GitHub issue and its acceptance criteria.
5. Approved Figma frames for visual intent only.
6. Current repository code, schema, migrations, and tests for implemented behavior.
7. Accepted research outputs.
8. Reference documents.
9. Chat history.

Chat is a working context, not the canonical project state.

## Required reading

Before consequential work, read only the material relevant to the task, beginning with:

1. `docs/PROJECT_BRIEF.md`
2. `docs/DECISIONS.md`
3. `docs/MVP_SCOPE.md`
4. `docs/AI_AGENT_WORKFLOW.md`
5. `docs/SOURCE_POLICY.md` and `docs/VERIFICATION_POLICY.md` when data is involved
6. `docs/UI_UX_FIGMA_WORKFLOW.md` when product design or frontend work is involved
7. The active issue, task contract, and affected repository files

Avoid pasting the entire project history into every prompt.

## Current stage

**Status: PLANNING**

- Product requirements, competitor-pattern analysis, Figma design, data calibration, schema design, architecture, security planning, and implementation backlog work are authorized.
- Production application implementation is not yet authorized.
- A bounded technical spike is allowed only when an approved planning issue states its purpose, limits, and disposal or promotion criteria.
- Do not scaffold a production application merely because the repository exists.

## Dynamic agent assignment

Every consequential issue should state:

- primary agent;
- human owner;
- mode: research, planning, design, implementation, debugging, or review;
- Fresh or Existing context when relevant;
- branch or worktree;
- binding constraints;
- acceptance evidence;
- permissions;
- review trigger.

Use one primary owner per issue. Parallel agents may work only on separable workstreams or against a frozen shared interface.

## Review policy

Independent review is risk-triggered, not ceremonial. Strong triggers include:

- authentication, authorization, or Supabase Row Level Security;
- sensitive data or location privacy;
- immutable fact history, provenance, or corrections;
- new public mutation endpoints;
- foundational schema or cross-layer contracts;
- significant dependency, security, or deployment changes;
- behavior poorly observed by ordinary tests;
- large or surprising implementations.

Routine documentation and low-risk isolated changes do not automatically require a second-agent review.

## Non-negotiable product constraints

- Toronto first; do not silently broaden public scope to Ontario or Canada.
- Prefer complete, trustworthy profiles over maximum listing count.
- Preserve `present`, `absent`, and `unknown` as distinct states.
- Every important gym fact must support provenance and an observation date.
- User submissions must not overwrite approved facts directly.
- Open-ended gym reviews are outside the MVP.
- Google Maps scraping and Reddit ingestion are prohibited product-data strategies.
- Gym-operator contact is optional and non-blocking.
- Payments, automated rewards, paid placement, real-time crowding, and native mobile apps are outside the MVP.
- Matching must remain deterministic and explainable at MVP stage.

## Figma boundary

- Figma is the workspace for information architecture, flows, wireframes, design foundations, components, prototypes, and visual handoff.
- Figma does not override product scope, verification rules, security constraints, or database semantics.
- Approved Figma frames define visual intent; accepted requirements define behavior; tested code defines runtime behavior.
- Competitor products may inform patterns, but their branding, assets, copy, and complete compositions must not be copied.

## Engineering constraints

- Enforce authorization, privileged-field protection, and rate limits at the server or database layer.
- Never expose service credentials in browser code.
- Prefer the simplest architecture that satisfies accepted requirements.
- Keep the MVP viable near a zero-dollar operating budget.
- Do not introduce a paid dependency without documenting free limits, lock-in risk, and fallback.
- Do not add a dependency merely to avoid writing a small, clear function.
- Validate and sanitize user-controlled input.
- Treat uploaded files as untrusted.
- Use synthetic or explicitly marked fixture data during development.
- Include tests or reproducible verification for every behavior change.

## Git preflight and permissions

Before consequential editing, verify:

- repository root;
- active branch;
- current HEAD when supplied;
- staged, unstaged, and untracked state;
- active issue and authority.

If the starting state materially differs from the task contract, stop. Do not automatically reset, stash, clean, switch branches, or repair history.

No implicit permission exists for:

- pushing;
- opening or merging a pull request;
- deployment;
- hosted-service mutation;
- destructive database work;
- secrets changes;
- dependency additions or mass upgrades.

The task or human owner must authorize these actions explicitly.

## Change discipline

Before editing:

1. State the issue or outcome.
2. List the expected files or boundaries.
3. Identify unrecorded assumptions.
4. State permissions and exclusions.

After editing:

1. Summarize the outcome.
2. List files changed and why.
3. Report focused and broader evidence.
4. Report failures and their classification.
5. Confirm what did not change.
6. List remaining uncertainty.
7. Return an exact status such as `PLANNING`, `IMPLEMENTED — REVIEW PENDING`, `CORRECTION REQUIRED`, or `CLOSED`.

## Decision discipline

Do not change scope, source hierarchy, verification semantics, canonical data ownership, Figma truth boundaries, agent governance, or the provisional stack without updating `docs/DECISIONS.md`. Add or supersede an ADR for a significant change.

## Data integrity

Never invent a gym attribute, equipment model, manufacturer, count, price, opening hour, source, or verification event. Missing evidence remains `unknown`. Test fixtures must be clearly fictional or marked as fixtures.
