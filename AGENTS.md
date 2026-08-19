# AGENTS.md — Coding-Agent Instructions

These instructions apply to Codex and any other coding agent working in this repository.

## Required reading order

Before proposing or changing implementation:

1. `docs/PROJECT_BRIEF.md`
2. `docs/DECISIONS.md`
3. `docs/MVP_SCOPE.md`
4. `docs/SOURCE_POLICY.md`
5. `docs/VERIFICATION_POLICY.md`
6. The active GitHub issue and its acceptance criteria

## Current stage

This project is in discovery and pre-planning. Do not scaffold a production application merely because the repository exists. Implementation begins only through an approved issue.

## Non-negotiable product constraints

- Toronto first; do not silently broaden public scope to Ontario or Canada.
- Optimize for complete, trustworthy profiles rather than maximum listing count.
- Preserve `unknown`, `confirmed absent`, and `confirmed present` as distinct states.
- Every important gym fact must support provenance and an observation date.
- User submissions must not overwrite approved facts directly.
- Open-ended gym reviews are outside the MVP.
- Google Maps scraping and Reddit ingestion are prohibited data-source strategies.
- Gym-operator contact is optional and non-blocking.
- Payments, automated rewards, real-time crowding, and native mobile apps are outside the MVP.

## Engineering constraints

- Enforce authorization, privileged-field protection, and rate limits at the server/database layer.
- Never expose service credentials in browser code.
- Prefer the simplest architecture that satisfies accepted requirements.
- Keep the project viable near a zero-dollar operating budget during MVP validation.
- Do not introduce a new paid dependency without documenting the free limits, lock-in risk, and fallback.
- Do not add a dependency merely to avoid writing a small, clear function.
- Validate and sanitize user-controlled input.
- Treat uploaded files as untrusted.
- Include tests or reproducible manual verification steps for every behavior change.

## Change discipline

Before editing:

1. State the issue being addressed.
2. List the files expected to change.
3. Identify any decision or assumption that is not already recorded.

After editing:

1. Summarize the behavior changed.
2. Report tests and verification performed.
3. List unresolved risks or assumptions.
4. Update documentation when behavior or architecture changed.

## Decision discipline

Do not change scope, the source hierarchy, verification semantics, canonical data ownership, or the provisional stack without updating `docs/DECISIONS.md` and, for a significant change, adding an ADR under `docs/decisions/`.

## Data integrity

Never invent a gym attribute, equipment model, manufacturer, count, price, opening hour, or verification event. Test fixtures must be clearly fictional or marked as fixtures.
