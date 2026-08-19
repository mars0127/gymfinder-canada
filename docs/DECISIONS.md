# Decision Log

This is the authoritative summary of product and technical decisions. Significant decisions also have individual records in `docs/decisions/`.

## Status definitions

- **Accepted:** Follow this decision unless it is formally superseded.
- **Provisional:** Use for current work, but validate before the formal project plan is frozen.
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
| D-005 | Accepted | Gym-operator contact and participation are non-blocking and deferred. | The project must be viable without partnerships, staff dashboards, or operator responses. | [ADR-0005](decisions/ADR-0005-operator-contact-nonblocking.md) |
| D-006 | Accepted | Validation must be tied to a named decision; ceremonial interviews are prohibited. | Research is useful only when it can alter scope, design, or priorities. | [ADR-0006](decisions/ADR-0006-decision-linked-validation.md) |
| D-007 | Provisional | Use TypeScript/Next.js and Supabase for the MVP unless the technical spike reveals a material problem. | Relational data, public pages, authentication, and row-level authorization fit the product. | [ADR-0007](decisions/ADR-0007-provisional-stack.md) |
| D-008 | Accepted | Keep the repository private and unlicensed initially. | Product, ownership, and open-source strategy are not yet settled. | [ADR-0008](decisions/ADR-0008-private-repository-no-license-yet.md) |
| D-009 | Accepted | Browsing does not require an account; contributing may require one. | Users should experience value before being asked to register. | — |
| D-010 | Accepted | Preserve `present`, `absent`, and `unknown` as distinct states. | Missing data must not create false exclusions or recommendations. | — |
| D-011 | Accepted | Do not use Google Maps scraping or Reddit ingestion for the product dataset. | Platform restrictions, provenance, deletion obligations, and long-term dependency risk are unacceptable for the MVP. | — |
| D-012 | Accepted | Do not include payments, subscriptions, automated trial rewards, or paid placement in the MVP. | These do not test the core data and matching hypothesis. | — |
| D-013 | Accepted | Matching must be explainable and deterministic at MVP stage. | Reliable filters are preferable to opaque AI scores built on incomplete data. | — |
| D-014 | Accepted | User submissions cannot directly overwrite approved facts. | Protects against mistakes, abuse, and coordinated data manipulation. | — |
| D-015 | Accepted | One founder/agent implements; the other founder/agent reviews important changes. | Reduces shared blind spots and prevents two AI systems from silently diverging. | — |

## Open decisions before the formal project plan

| ID | Decision needed | Evidence required | Owner |
|---|---|---|---|
| O-001 | Exact seed geography within Toronto. | Ten-gym audit coverage and founder accessibility. | Founders |
| O-002 | Canonical location seed source. | Overture/OSM/Toronto/open-web source comparison. | Research owner |
| O-003 | Final P0 attribute set. | Availability audit plus task-based user evidence. | Product owner |
| O-004 | Initial equipment taxonomy depth. | Search use cases and data availability. | Product + data owner |
| O-005 | Whether evidence photos are private-to-moderators or publicly displayed. | Privacy, copyright, moderation, and storage review. | Founders |
| O-006 | Whether an interactive map is necessary at launch. | Task testing and cost/usability comparison. | UX owner |
| O-007 | Exact profile completeness threshold. | Ten-gym audit results. | Founders |
| O-008 | Final authentication timing and provider configuration. | Technical spike and contribution-flow design. | Technical owner |
| O-009 | Public product name and domain. | Deferred until core product plan is accepted. | Founders |

## Decision workflow

1. State the decision and why it matters.
2. Identify the cheapest evidence that could change the answer.
3. Record the chosen option, alternatives, consequences, and review trigger.
4. Update this table.
5. Add or update an ADR when the impact is significant.
