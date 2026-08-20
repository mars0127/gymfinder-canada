# Initial Planning Backlog

Create these as GitHub issues after the Stage 1 governance patch is merged. The current phase uses ChatGPT and/or Codex for planning. Codex and Claude become peer agents after implementation is authorized.

## Issue 1 — Merge Stage 1 governance and workspace alignment

**Type:** Documentation / decision

### Objective

Make the repository accurately represent the accepted planning, agent, Figma, and evidence workflow.

### Acceptance criteria

- [ ] `AGENTS.md` contains the shared policy.
- [ ] `CLAUDE.md` no longer restricts Claude to review.
- [ ] Peer-agent and planning-control decisions are recorded.
- [ ] Figma workflow is recorded.
- [ ] External user testing is removed from the planning gate.
- [ ] Five-gym calibration replaces the ten-gym audit requirement.
- [ ] Planning templates and roadmap are present.
- [ ] Repository access for both founders is confirmed.
- [ ] Private-repository access is granted to the GitHub integration used for later inspections, when desired.

### Exclusions

- No production application code.
- No competitor audit execution.
- No Figma screen creation.

---

## Issue 2 — Complete the competitor UX pattern audit

**Type:** Planning research / UX

### Objective

Extract reusable discovery, filtering, comparison, profile, trust, and correction patterns from direct and adjacent products.

### Acceptance criteria

- [ ] Candidate products and exact flows are recorded.
- [ ] Sources and retrieval dates are present.
- [ ] Each pattern has strengths and weaknesses.
- [ ] Each pattern receives `adopt`, `adapt`, `reject`, or `defer`.
- [ ] No proprietary branding, copy, assets, or full layouts are copied.
- [ ] Findings are reflected on the Figma competitor-pattern page.
- [ ] Final synthesis identifies the recommended GymFinder interaction model.

---

## Issue 3 — Draft and accept PRD v1

**Type:** Product planning

### Objective

Convert accepted decisions and competitor-pattern findings into a complete MVP product contract.

### Acceptance criteria

- [ ] Target user, problem, jobs, and use cases are defined.
- [ ] Functional requirements and non-goals are explicit.
- [ ] Must-have versus preferred matching is defined.
- [ ] Unknown-state behavior is defined.
- [ ] Search, results, comparison, profile, correction, and moderation requirements are defined.
- [ ] Assumptions unvalidated by live use are listed.
- [ ] Pilot success, pause, and revision criteria are defined.
- [ ] Founders accept PRD v1.

---

## Issue 4 — Create the Figma planning and design baseline

**Type:** Product design

### Objective

Create the information architecture, critical flows, wireframes, foundations, components, high-fidelity screens, prototype, and handoff baseline.

### Acceptance criteria

- [ ] Figma project/file access is configured.
- [ ] Required pages follow `UI_UX_FIGMA_WORKFLOW.md`.
- [ ] Information architecture is complete.
- [ ] Critical flows are complete.
- [ ] Mobile and desktop low-fidelity wireframes are complete.
- [ ] Unknown, stale, disputed, loading, empty, and error states are covered.
- [ ] Design foundations and initial components are defined.
- [ ] Critical high-fidelity screens and prototype are accepted.
- [ ] Handoff annotations link to relevant requirements.

---

## Issue 5 — Complete the five-gym data calibration

**Type:** Data planning research

### Objective

Ensure the P0 fields, source strategy, and schema reflect obtainable real-world data.

### Acceptance criteria

- [ ] Five varied Toronto facilities are included.
- [ ] Present, absent, and unknown are distinct.
- [ ] Every populated fact has a source and date.
- [ ] Contradictions, duplicates, and closure uncertainty are recorded.
- [ ] Collection and maintenance difficulty are recorded.
- [ ] Operator contact is not required.
- [ ] Required, optional, and deferred attributes are recommended.
- [ ] A provisional canonical-source strategy is recommended.

---

## Issue 6 — Define the data model and trust architecture

**Type:** Data / architecture planning

### Objective

Define gym identity, source records, equipment, facts, evidence, freshness, corrections, disputes, moderation, and completeness.

### Acceptance criteria

- [ ] Canonical gyms and source records are separate.
- [ ] Equipment type, manufacturer, model, loading type, and quantity can be represented.
- [ ] Present, absent, and unknown are distinct.
- [ ] Provenance and dates are retained.
- [ ] Corrections preserve history.
- [ ] Conflicts and disputes are representable.
- [ ] Freshness and completeness are defined.
- [ ] Representative matching queries can be expressed.
- [ ] A bounded spike is used only if necessary.

---

## Issue 7 — Define technical architecture, security, privacy, and testing

**Type:** Technical planning

### Objective

Create a buildable near-zero-cost architecture with explicit trust and operational boundaries.

### Acceptance criteria

- [ ] Framework and repository structure are defined.
- [ ] Supabase and hosting assumptions are verified through current primary sources.
- [ ] Server/client and RLS boundaries are defined.
- [ ] Authentication timing is decided.
- [ ] Mapping, storage, caching, deployment, and backup approaches are defined.
- [ ] Security and privacy baseline is complete.
- [ ] Accessibility requirements are complete.
- [ ] Test and evidence strategy is complete.
- [ ] Paid dependencies and free-tier assumptions are documented.

---

## Issue 8 — Integrate and freeze the build-ready planning package

**Type:** Planning integration / decision

### Objective

Reconcile the PRD, Figma, data model, verification policy, and technical architecture.

### Acceptance criteria

- [ ] Cross-document contradictions are resolved.
- [ ] Open decisions O-001 through O-008 are accepted or explicitly deferred.
- [ ] P0 attributes and completeness threshold are accepted.
- [ ] Seed-source strategy is accepted.
- [ ] Map requirement is accepted or deferred.
- [ ] Evidence-photo policy is accepted or deferred.
- [ ] MVP scope is frozen.
- [ ] Relevant ADRs are added or superseded.

---

## Issue 9 — Create implementation backlog and planning closeout

**Type:** Delivery planning

### Objective

Produce dependency-ordered implementation issues and a durable recovery capsule.

### Acceptance criteria

- [ ] Implementation epics are ordered by dependency.
- [ ] Each issue includes owner, primary agent, mode, branch, dependencies, evidence, permissions, and review trigger.
- [ ] Codex and Claude assignments remain interchangeable and task-based.
- [ ] High-risk boundaries have independent-review plans.
- [ ] Pilot launch and measurement plan is complete.
- [ ] Planning closeout records the accepted checkpoint and next safe action.
- [ ] Founders explicitly authorize or withhold implementation.
