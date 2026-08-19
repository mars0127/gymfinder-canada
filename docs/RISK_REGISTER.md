# Risk Register

Ratings are qualitative and should be revisited when evidence changes.

| ID | Risk | Likelihood | Impact | Current mitigation | Trigger for review |
|---|---|---:|---:|---|---|
| R-001 | Core equipment data is unavailable or too costly to maintain. | High | Critical | Ten-gym audit; reduce P0 attributes; local depth. | Fewer than most P0 fields can be resolved without prohibited sources. |
| R-002 | Profiles become stale and produce incorrect recommendations. | High | Critical | Per-fact dates, recheck intervals, stale labels, correction workflow. | A meaningful share of beta corrections concerns old information. |
| R-003 | Duplicate, moved, rebranded, or closed gyms split evidence. | Medium | High | Canonical gym entity plus separate source records and aliases. | Audit finds repeated duplicate or closure conflicts. |
| R-004 | Source terms or licences restrict storage or reuse. | Medium | High | Source policy, provenance ledger, no Google/Reddit ingestion, source separation. | New automated source or bulk import is proposed. |
| R-005 | Fake accounts or coordinated submissions poison equipment data. | Medium | Critical | Pending moderation, server-side limits, append-only verification history. | Public contributions open or rewards are proposed. |
| R-006 | Product depends on gym-operator cooperation that founders cannot obtain. | Low | High | Operator participation explicitly non-blocking; no staff dashboard in MVP. | A planned feature cannot function without operator data. |
| R-007 | Broad scope prevents completion. | High | High | Toronto-first, explicit exclusions, scope-change rule, decision log. | Ontario/Canada expansion or adjacent marketplace features enter an issue. |
| R-008 | Open-ended content creates moderation and defamation burden. | Medium | High | No open reviews in MVP; structured factual corrections only. | Reviews, comments, or public notes are proposed. |
| R-009 | Precise location or uploads create privacy harm. | Medium | High | No stored location history by default; limited evidence; metadata stripping; private notes. | Geolocation history or public evidence gallery is proposed. |
| R-010 | Free-tier limits or abuse create unexpected cost. | Medium | High | List-first UI, limited images, usage caps, no paid API dependency. | A paid service or high-volume map/image feature is proposed. |
| R-011 | AI agents fabricate data or silently redesign the system. | Medium | Critical | AGENTS.md, source-of-truth hierarchy, ADRs, human review, fixtures clearly marked. | AI-generated seed data or unreviewed architecture change appears. |
| R-012 | Two founders and two AI tools create conflicting branches and decisions. | High | Medium | Issues first, one branch per task, one implementer/one reviewer, decision log. | Duplicate implementation or conflicting documents appear. |
| R-013 | The target segment is too narrow or exact equipment rarely changes choices. | Medium | High | Decision-linked task tests; preserve ability to expand later. | Task evidence shows distance and price dominate nearly every choice. |
| R-014 | Accessibility or privacy is retrofitted too late. | Medium | High | Accessible list-first UX; minimal collection; baseline requirements in plan. | First interactive prototype is designed. |

## Risk-review rule

A pull request must update this register when it:

- introduces a new data source;
- adds user-generated content;
- stores precise location or images;
- introduces a paid service;
- changes public scope;
- adds gym staff permissions;
- changes authentication or authorization;
- changes the source of canonical gym identity.
