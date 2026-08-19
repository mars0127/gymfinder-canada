# Contributing

This repository is shared by two founders using ChatGPT/Codex during planning and Codex plus Claude as peer implementation agents after implementation is authorized.

## Project status

Current status: **PLANNING**

Planning artifacts, bounded research, Figma work, data calibration, architecture design, and explicitly approved spikes are allowed. Production feature implementation begins only after the build-ready planning package is accepted.

## Issues first

Substantial work begins with a GitHub issue containing:

- Task ID or issue number;
- intended outcome or decision;
- human owner;
- primary agent, when assigned;
- work mode;
- scope and exclusions;
- dependencies and frozen interfaces;
- acceptance evidence;
- remote or destructive permissions;
- review trigger.

Use the templates under `.github/ISSUE_TEMPLATE/`.

## Branches

Use one branch per task:

```text
planning/<short-description>
design/<short-description>
research/<short-description>
spike/<short-description>
feat/<short-description>
fix/<short-description>
security/<short-description>
chore/<short-description>
```

Examples:

```text
planning/prd-v1
design/search-and-results-flow
research/five-gym-data-calibration
spike/fact-provenance-model
feat/gym-filter-query
security/contribution-rls
```

Two agents must not edit the same branch simultaneously.

## Dynamic human and AI roles

- Human founders retain product authority and approve significant decisions and merges.
- During planning, ChatGPT and/or Codex may supervise, research, draft, reconcile, and maintain continuity.
- During implementation, Codex and Claude are peer agents. Either can own any workstream.
- Each issue has one primary agent or human owner.
- Review responsibility rotates and is required only where risk or information value justifies it.
- Parallel work requires independent boundaries or a frozen shared interface.

AI agreement is not proof. Agent reports are claims to verify against the repository and appropriate evidence.

## Task and run identity

For ordinary low-risk work, the GitHub issue and branch are enough.

For high-risk, long-running, or multi-agent work, also record:

- context ID;
- prompt or contract version;
- run ID;
- starting repository checkpoint.

Use `docs/templates/AGENT_TASK_CONTRACT.md` and `docs/templates/AGENT_RUN_REPORT.md` when this traceability is useful. Do not create bureaucracy for trivial edits.

## Pull requests

- Keep each pull request focused on one issue.
- Link the issue.
- Identify the primary agent and work mode.
- Explain what changed and why.
- Verify every acceptance criterion.
- Include tests, build evidence, screenshots, Figma links, or reproducible manual steps as appropriate.
- Explicitly identify schema, privacy, security, source-policy, Figma, dependency, and cost impact.
- State remote or destructive actions performed; use `None` when none occurred.
- State whether independent review is required and why.
- Do not mix unrelated refactors with a product feature.

## Figma workflow

Use `docs/UI_UX_FIGMA_WORKFLOW.md` for design work.

- Link the relevant Figma page or frame in the issue and pull request.
- Record the approved visual state or frame version before implementation.
- Update Figma, the requirement, or the implementation when a material divergence is accepted.
- Never copy competitor logos, proprietary artwork, marketing copy, or a complete screen composition.

## Decision changes

Update `docs/DECISIONS.md` when a decision changes. Add an ADR under `docs/decisions/` when the change affects:

- target users or geography;
- MVP boundaries;
- source licensing or scraping;
- canonical data model;
- verification or moderation;
- authentication and authorization;
- Figma truth boundaries or design system;
- agent governance;
- infrastructure or paid dependencies.

## Research and planning evidence

- Separate direct observation from interpretation.
- Record source references and retrieval dates.
- Do not copy restricted platform content into the product dataset.
- Do not infer `absent` from missing evidence.
- External user interviews and usability testing are deferred until a prototype or alpha unless a founder explicitly reopens them.
- Gym-operator participation is not a planning dependency.

## Secrets and private data

Never commit:

- `.env` files;
- API keys;
- service-role credentials;
- database passwords;
- private authentication tokens;
- raw participant identities or contact details;
- precise private locations;
- unredacted sensitive data.
