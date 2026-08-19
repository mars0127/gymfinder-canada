# GymFinder Canada

A Toronto-first gym discovery and comparison project focused on exact equipment, equipment manufacturers, amenities, access policies, and transparent verification.

> **Project stage:** Discovery and pre-planning. No production application has been selected or implemented yet.

## Current product thesis

People choosing a gym often cannot determine whether a specific location has the equipment or facilities they need. Existing information is fragmented across gym websites, maps, photos, reviews, and informal community discussions. GymFinder aims to make those facts structured, comparable, traceable, and correctable.

The current MVP candidate is deliberately narrow:

- City of Toronto first, with an operational focus on locations the founders can realistically research.
- Strength-training users first.
- Approximately 30–50 complete profiles rather than thousands of empty listings.
- Structured gym facts and corrections rather than open-ended reviews.
- A visible source, observation date, and verification status for important facts.
- No payments, automated trial rewards, real-time crowding, or Canada-wide launch in the MVP.

## Start here

1. Read [`docs/PROJECT_BRIEF.md`](docs/PROJECT_BRIEF.md).
2. Review accepted and provisional decisions in [`docs/DECISIONS.md`](docs/DECISIONS.md).
3. Read [`docs/NEXT_STEPS_TO_PROJECT_PLANNING.md`](docs/NEXT_STEPS_TO_PROJECT_PLANNING.md).
4. Publish this repository privately and invite the second founder using [`SETUP_GITHUB.md`](SETUP_GITHUB.md).
5. Open the initial issues listed in [`docs/INITIAL_BACKLOG.md`](docs/INITIAL_BACKLOG.md).

## Repository structure

```text
.
├── .github/                  # Issue and pull-request templates
├── docs/                     # Product, research, trust, and planning documents
│   ├── decisions/            # Architecture/product decision records (ADRs)
│   └── templates/            # Reusable research and decision templates
├── references/               # Private project reference material
├── research/                 # Sanitized audit and task-test outputs
├── AGENTS.md                 # Codex and coding-agent operating rules
├── CLAUDE.md                 # Claude operating rules
├── CONTRIBUTING.md           # Two-founder collaboration workflow
└── SETUP_GITHUB.md           # Publishing and collaborator setup
```

## Source of truth

When documents conflict, use this order:

1. Accepted entries in `docs/DECISIONS.md` and accepted ADRs.
2. `docs/MVP_SCOPE.md`.
3. `docs/PROJECT_BRIEF.md`.
4. Current GitHub issue acceptance criteria.
5. Research notes and reference documents.
6. AI chat history.

Chat history is never the authoritative project record. Important decisions must be committed to the repository.

## Working rules

- Do not infer or fabricate gym facts.
- Treat `unknown` as different from `no`.
- Do not scrape Google Maps or ingest Reddit content into the product database.
- Do not add open-ended reviews to the MVP.
- Do not make gym-operator participation a prerequisite for planning or launch.
- Do not conduct interviews merely to satisfy a process. Validation must answer a named decision.
- Do not merge major scope, schema, security, or source-policy changes without a decision record.

## Reference report

The original comprehensive discussion report is retained in `references/` as a product, legal, and cybersecurity reference. It is not the final requirements specification.
