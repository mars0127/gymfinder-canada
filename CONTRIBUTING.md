# Contributing

This repository is shared by two founders using ChatGPT/Codex and Claude as development assistants.

## Branches

Use one branch per task:

```text
research/<short-description>
docs/<short-description>
feat/<short-description>
fix/<short-description>
chore/<short-description>
```

Examples:

```text
research/ten-gym-source-audit
docs/update-verification-policy
feat/gym-filter-query
fix/unknown-equipment-state
```

## Issues first

Substantial work begins with a GitHub issue containing:

- problem or decision;
- scope;
- acceptance criteria;
- exclusions;
- dependencies;
- verification method.

Use the templates under `.github/ISSUE_TEMPLATE/`.

## Pull requests

- Keep each pull request focused on one issue.
- Link the issue in the pull-request description.
- Explain what changed and why.
- Include tests or manual verification steps.
- Explicitly identify schema, privacy, security, source-policy, and cost impact.
- Do not mix unrelated refactors with a product feature.

## Human and AI roles

A useful default is:

1. One founder defines the issue and acceptance criteria.
2. One AI agent helps implement or draft.
3. The other founder and/or the other AI agent reviews critically.
4. A human founder makes the final decision.

AI agreement is not evidence that a product decision is correct.

## Decision changes

Update `docs/DECISIONS.md` when a decision changes. Add an ADR under `docs/decisions/` when the change affects:

- target users or geography;
- MVP boundaries;
- source licensing or scraping;
- canonical data model;
- verification or moderation;
- authentication and authorization;
- infrastructure or paid dependencies.

## Research data

- Commit sanitized observations, not participant identities.
- Do not commit private email addresses, phone numbers, precise user locations, or recordings.
- Do not copy restricted platform content into the repository.
- Record source references and dates.
- Separate observed evidence from founder interpretation.

## Secrets

Never commit:

- `.env` files;
- API keys;
- service-role credentials;
- database passwords;
- private authentication tokens;
- unredacted personal data.
