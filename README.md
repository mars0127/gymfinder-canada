# GymFinder Canada

A Toronto-first gym discovery and comparison project focused on exact equipment, equipment manufacturers, amenities, access policies, and transparent verification.

> **Project status:** `PLANNING`. Production application implementation is not yet authorized.

## Current product thesis

People choosing a gym often cannot determine whether a specific location has the equipment or facilities they need. Existing information is fragmented across gym websites, maps, photos, reviews, and informal community discussions. GymFinder aims to make those facts structured, comparable, traceable, and correctable.

The current MVP candidate is deliberately narrow:

- City of Toronto first.
- Strength-training users first.
- Approximately 30–50 complete profiles rather than thousands of empty listings.
- Structured gym facts and corrections rather than open-ended reviews.
- A visible source, observation date, and verification status for important facts.
- No payments, automated trial rewards, real-time crowding, or Canada-wide launch in the MVP.

## Current workflow

- Pre-implementation planning is conducted with ChatGPT and/or Codex under the current owner decision.
- Figma is used for information architecture, flows, wireframes, components, prototypes, and handoff.
- External user testing and gym-operator outreach are not planning prerequisites.
- A five-gym data calibration informs the filter set and schema during planning.
- After implementation is authorized, Codex and Claude are peer agents with roles assigned per issue.

## Start here

1. Read [`docs/PROJECT_BRIEF.md`](docs/PROJECT_BRIEF.md).
2. Review [`docs/DECISIONS.md`](docs/DECISIONS.md).
3. Read the [`build-ready planning roadmap`](docs/NEXT_STEPS_TO_PROJECT_PLANNING.md).
4. Read the [`AI-agent workflow`](docs/AI_AGENT_WORKFLOW.md).
5. Read the [`Figma UI/UX workflow`](docs/UI_UX_FIGMA_WORKFLOW.md).
6. Use [`docs/INITIAL_BACKLOG.md`](docs/INITIAL_BACKLOG.md) to create planning issues.

## Repository structure

```text
.
├── .github/                  # Issue and pull-request templates
├── docs/                     # Product, planning, design, trust, and architecture documents
│   ├── decisions/            # Architecture/product decision records
│   └── templates/            # Reusable agent, review, and research templates
├── references/               # Internal reference material
├── research/                 # Sanitized planning evidence
├── AGENTS.md                 # Shared instructions for all AI agents
├── CLAUDE.md                 # Claude-specific supplement
├── CONTRIBUTING.md           # Founder and agent contribution workflow
└── SETUP_GITHUB.md           # Access and local repository setup
```

## Source of truth

When documents conflict, use this order:

1. Accepted entries in `docs/DECISIONS.md` and accepted ADRs.
2. Accepted PRD and `docs/MVP_SCOPE.md`.
3. `docs/PROJECT_BRIEF.md`.
4. Current GitHub issue acceptance criteria.
5. Approved Figma frames for visual intent.
6. Current code, schema, migrations, and tests after implementation begins.
7. Accepted research outputs and references.
8. AI chat history.

Important decisions must be committed to the repository.

## Working rules

- Do not infer or fabricate gym facts.
- Treat `unknown` as different from `absent`.
- Do not scrape Google Maps or ingest Reddit content into the product database.
- Do not add open-ended reviews to the MVP.
- Do not make gym-operator participation a prerequisite for planning or launch.
- Do not conduct interviews merely to satisfy a process.
- Use competitor products as pattern evidence without copying their branding, assets, copy, or complete layouts.
- Do not merge major scope, schema, security, source-policy, Figma, or agent-governance changes without a decision record.

## Reference documents

The original GymFinder discussion report and the Human-Directed AI-Native Software Development Method are retained in `references/`. They are background and workflow references; accepted repository decisions remain authoritative.
