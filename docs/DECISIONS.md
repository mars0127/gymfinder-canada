# Decision Log

This is the authoritative summary of product, planning, design, and technical decisions. Significant decisions also have individual records in `docs/decisions/`.

## Status definitions

- **Accepted:** Follow this decision unless it is formally superseded.
- **Provisional:** Use for current work, but verify before the build-ready plan is frozen.
- **Deferred:** Deliberately postponed; not an accidental omission.
- **Rejected:** Considered and intentionally not selected.
- **Open:** Requires a decision.

## Current decisions

| ID | Status | Decision | Rationale | Record |
|---|---|---|---|---|
| D-001 | Accepted | Launch Toronto-first, not Canada-wide. | Local depth and maintenance are more valuable than empty national coverage. | [ADR-0001](decisions/ADR-0001-toronto-first.md) |
| D-002 | Provisional | Serve strength-training users first. | Exact equipment and manufacturer data create the clearest initial differentiation. | [ADR-0002](decisions/ADR-0002-strength-users-first.md) |
| D-003 | Accepted | Model and verify facts individually. | A gym-level verification badge cannot accurately represent mixed-source, differently aged facts. | [ADR-0003](decisions/ADR-0003-fact-level-data-model.md) |
| D-004 | Accepted | Use structured confirmations and corrections; exclude open-ended reviews from the MVP. | Reduces moderation and defamation exposure while preserving the core data loop. | [ADR-0004](decisions/ADR-0004-structured-contributions-no-open-reviews.md) |
| D-005 | Accepted | Gym-operator contact and participation are non-blocking and deferred. | The product must be viable without partnerships, staff dashboards, or operator responses. | [ADR-0005](decisions/ADR-0005-operator-contact-nonblocking.md) |
| D-006 | Accepted | Research must be tied to a named decision; ceremonial interviews are prohibited. | Evidence gathering is useful only when it can alter scope, design, or priorities. | [ADR-0006](decisions/ADR-0006-decision-linked-validation.md) |
| D-007 | Provisional | Use TypeScript/Next.js and Supabase for the MVP unless planning evidence reveals a material problem. | Relational data, public pages, authentication, and row-level authorization fit the product. | [ADR-0007](decisions/ADR-0007-provisional-stack.md) |
| D-008 | Accepted | Keep the repository private and unlicensed initially. | Product, ownership, and open-source strategy are not yet settled. | [ADR-0008](decisions/ADR-0008-private-repository-no-license-yet.md) |
| D-009 | Accepted | Browsing does not require an account; contributing may require one. | Users should experience value before registration. | — |
| D-010 | Accepted | Preserve `present`, `absent`, and `unknown` as distinct states. | Missing data must not create false exclusions or recommendations. | — |
| D-011 | Accepted | Do not use Google Maps scraping or Reddit ingestion for the product dataset. | Platform restrictions, provenance, deletion obligations, and dependency risk are unacceptable for the MVP. | — |
| D-012 | Accepted | Do not include payments, subscriptions, automated trial rewards, or paid placement in the MVP. | These do not test the core data and matching hypothesis. | — |
| D-013 | Accepted | Matching must be explainable and deterministic at MVP stage. | Reliable filters are preferable to opaque AI scores built on incomplete data. | — |
| D-014 | Accepted | User submissions cannot directly overwrite approved facts. | Protects against mistakes, abuse, and coordinated manipulation. | — |
| D-015 | Accepted | Codex and Claude are peer implementation agents; task ownership and review roles are assigned per issue. | Dynamic assignment uses each agent where it currently fits best and avoids wasting either tool. Independent review is risk-triggered. | [ADR-0009](decisions/ADR-0009-peer-agent-and-planning-control-model.md) |
| D-016 | Accepted | Conduct current pre-implementation planning through ChatGPT and/or Codex; Claude enters the default workflow when implementation is authorized. | The owner wants planning continuity here while preserving both agents for software delivery. | [ADR-0009](decisions/ADR-0009-peer-agent-and-planning-control-model.md) |
| D-017 | Accepted | Use Figma as the visual design, prototyping, and developer-handoff workspace. | It provides a durable shared design surface without making visual files authoritative over product, data, or security rules. | [ADR-0010](decisions/ADR-0010-figma-design-workspace.md) |
| D-018 | Accepted | Defer external user interviews and usability testing until a prototype or functional alpha. | They are not required to create the initial build-ready plan and would slow the current planning objective. | [ADR-0011](decisions/ADR-0011-competitor-patterns-and-deferred-user-testing.md) |
| D-019 | Accepted | Use comparable products as UX-pattern evidence, not as designs or datasets to copy. | Existing products can reduce avoidable UX invention while preserving independent branding and product decisions. | [ADR-0011](decisions/ADR-0011-competitor-patterns-and-deferred-user-testing.md) |
| D-020 | Accepted | Run a five-gym data-feasibility calibration during planning; it is not a gate to begin planning and requires no operator contact. | Real examples are needed to prevent a fictional schema and filter set, but a large audit is unnecessary now. | [ADR-0012](decisions/ADR-0012-five-gym-data-calibration.md) |
| D-021 | Accepted | Project status is `PLANNING`; production implementation is not authorized until the build-ready planning package is accepted. | Separates design and architecture decisions from premature application code. | [ADR-0009](decisions/ADR-0009-peer-agent-and-planning-control-model.md) |

## Open decisions before implementation authorization

| ID | Decision needed | Planning input | Owner |
|---|---|---|---|
| O-001 | Exact initial seed geography within Toronto. | Five-gym calibration and founder accessibility. | Founders |
| O-002 | Canonical location seed source. | Overture, OSM, Toronto Open Data, and first-party source comparison. | Data planning owner |
| O-003 | Final P0 attribute set. | Data calibration, competitor patterns, and founder product judgment. | Product owner |
| O-004 | Initial equipment-taxonomy depth. | Search requirements and real source granularity. | Product + data owner |
| O-005 | Whether evidence photos are moderator-only or publicly displayed. | Privacy, copyright, moderation, Figma, and storage review. | Founders |
| O-006 | Whether an interactive map is required at launch. | Competitor-pattern audit, Figma flows, list-first usability, and cost analysis. | UX owner |
| O-007 | Exact profile-completeness threshold. | Five-gym calibration. | Founders |
| O-008 | Final authentication timing and provider configuration. | Contribution-flow and technical-architecture planning. | Technical owner |
| O-009 | Public product name and domain. | Deferred until the core plan is accepted. | Founders |

## Decision workflow

1. State the decision and why it matters.
2. Identify the least expensive evidence that could materially change it.
3. Record the chosen option, alternatives, consequences, and review trigger.
4. Update this table.
5. Add or supersede an ADR when the impact is significant.
