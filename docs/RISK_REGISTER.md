# Risk Register

Ratings are qualitative and should be revisited when evidence changes.

| ID | Risk | Likelihood | Impact | Current mitigation | Trigger for review |
|---|---|---:|---:|---|---|
| R-001 | Core equipment data is unavailable or too costly to maintain. | High | Critical | Five-gym calibration; reduce P0 attributes; preserve unknown; prioritize local depth. | Candidate P0 fields cannot be resolved or maintained through permitted sources. |
| R-002 | Profiles become stale and produce incorrect recommendations. | High | Critical | Per-fact dates, recheck intervals, stale labels, and correction workflow. | A meaningful share of pilot corrections concerns old information. |
| R-003 | Duplicate, moved, rebranded, or closed gyms split evidence. | Medium | High | Canonical gym entity plus separate source records and aliases. | Calibration or seed import reveals repeated duplicate or closure conflicts. |
| R-004 | Source terms or licences restrict storage or reuse. | Medium | High | Source policy, provenance ledger, no Google/Reddit ingestion, and source separation. | A new automated source or bulk import is proposed. |
| R-005 | Fake accounts or coordinated submissions poison equipment data. | Medium | Critical | Pending moderation, server-side limits, append-only verification history, and risk-triggered security review. | Public contributions open or rewards are proposed. |
| R-006 | Product depends on gym-operator cooperation that founders cannot obtain. | Low | High | Operator participation is explicitly non-blocking; no staff dashboard in MVP. | A planned feature cannot function without operator data. |
| R-007 | Broad scope prevents completion. | High | High | Toronto-first scope, explicit exclusions, scope-change rule, and decision log. | Ontario/Canada expansion or adjacent marketplace features enter an issue. |
| R-008 | Open-ended content creates moderation and defamation burden. | Medium | High | No open reviews in MVP; structured factual corrections only. | Reviews, comments, or public free-text notes are proposed. |
| R-009 | Precise location or uploads create privacy harm. | Medium | High | No stored location history by default; limited evidence; metadata stripping; least collection. | Geolocation history or a public evidence gallery is proposed. |
| R-010 | Free-tier limits or abuse create unexpected cost. | Medium | High | List-first UI, limited images, usage caps, no paid API dependency, and budget-aware architecture review. | A paid service or high-volume map/image feature is proposed. |
| R-011 | AI agents fabricate data or silently redesign the system. | Medium | Critical | Shared `AGENTS.md`, task contracts, source-of-truth hierarchy, ADRs, human approval, and fictional fixtures. | AI-generated seed data or an unrecorded scope/schema change appears. |
| R-012 | Two founders and multiple AI contexts create conflicting branches, interfaces, or decisions. | High | High | One primary owner per issue, isolated branches/worktrees, frozen interfaces before parallel work, peer-agent policy, and repository recovery capsule. | Duplicate implementations, conflicting documents, or repeated handoff failures appear. |
| R-013 | Deferring external user testing causes incorrect UX or demand assumptions. | Medium | High | Competitor-pattern audit, founder product judgment, accessibility heuristics, explicit assumption log, and alpha/pilot measurement plan. | Prototype/alpha evidence contradicts planned behavior or users fail critical flows. |
| R-014 | Accessibility or privacy is retrofitted too late. | Medium | High | Accessible list-first design, Figma state/accessibility annotations, minimal collection, and planning baseline. | First interactive design or public data flow is approved without the required checks. |
| R-015 | Figma, PRD, schema, and production code diverge. | Medium | High | Truth-boundary rules, linked issues/frames, planning integration review, and documented material divergence. | A screen requires unavailable data or code behavior contradicts an approved flow. |
| R-016 | Agent-process overhead delays product delivery. | Medium | Medium | Use detailed contracts only for consequential work; risk-triggered review; anti-drag checkpoints. | Several governed runs occur without closing a meaningful planning or implementation boundary. |

## Risk-review rule

A pull request must update this register when it:

- introduces a new data source;
- adds user-generated content;
- stores precise location or images;
- introduces a paid service;
- changes public scope;
- adds gym staff permissions;
- changes authentication or authorization;
- changes canonical gym identity;
- changes Figma truth boundaries or the agent-governance model;
- defers or removes an evidence requirement that materially affects risk.
