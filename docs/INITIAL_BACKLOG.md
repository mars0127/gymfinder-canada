# Initial Backlog

Create these as GitHub issues after the repository is published.

## Issue 1 — Confirm founder alignment and repository ownership

**Type:** Documentation / decision

### Objective

Ensure both founders are working from the same product brief and decision log.

### Acceptance criteria

- [ ] Second founder has repository access.
- [ ] Both founders have reviewed the project brief, MVP scope, and decisions.
- [ ] Disagreements are documented as comments.
- [ ] Accepted changes are merged through a pull request.
- [ ] `COLLABORATION.md` contains both GitHub usernames.

### Exclusions

- No application code.
- No branding work.

---

## Issue 2 — Select the ten-gym audit sample

**Type:** Research

### Objective

Choose a varied Toronto sample that exposes data-source and attribute problems.

### Acceptance criteria

- [ ] Sample contains chain, independent strength, and municipal facilities.
- [ ] Sample includes North York and at least one other Toronto area.
- [ ] Sample includes at least one location with limited public information.
- [ ] Selection rationale is documented.
- [ ] No gym requires operator participation to remain in the sample.

---

## Issue 3 — Complete the ten-gym source and attribute audit

**Type:** Research

### Objective

Determine which P0 facts can be obtained, sourced, and maintained responsibly.

### Acceptance criteria

- [ ] Each gym has a completed audit record.
- [ ] Present, absent, and unknown are distinct.
- [ ] Every populated fact has a source and date.
- [ ] Contradictions and duplicates are recorded.
- [ ] Effort/difficulty is recorded.
- [ ] Audit concludes which attributes should remain P0, move to P1, or be removed.
- [ ] Audit recommends a provisional canonical seed source.

---

## Issue 4 — Validate the gym-selection task

**Type:** Research / UX

### Objective

Determine whether structured equipment and facility facts materially improve a real gym choice.

### Acceptance criteria

- [ ] Both founders complete an independent realistic selection task.
- [ ] Public problem evidence is summarized without becoming product data.
- [ ] Any remaining decision uncertainty is named.
- [ ] Up to three to five task tests are run only if needed.
- [ ] Final recommendation lists the most decision-critical attributes.

### Exclusions

- No generic “would you use this?” interview quota.
- No requirement to recruit strangers.

---

## Issue 5 — Build the data-model spike

**Type:** Technical discovery

### Objective

Prove that the proposed model can represent gym identity, sources, facts, equipment, uncertainty, corrections, conflicts, and matching.

### Acceptance criteria

- [ ] Canonical gyms are separate from source records.
- [ ] Equipment type, manufacturer, model, and quantity can be represented.
- [ ] Present, absent, and unknown are distinct.
- [ ] Approved facts retain provenance and dates.
- [ ] Corrections do not overwrite history.
- [ ] Conflicts can be represented.
- [ ] At least five representative filter queries work against fixtures.
- [ ] The spike documents whether the provisional stack remains suitable.

### Exclusions

- No production UI.
- No staff dashboard.
- No payments or rewards.

---

## Issue 6 — Freeze the MVP decisions

**Type:** Decision

### Objective

Convert audit, task, and spike evidence into accepted planning inputs.

### Acceptance criteria

- [ ] Open decisions O-001 through O-008 are resolved or explicitly deferred.
- [ ] P0 attributes and completeness threshold are accepted.
- [ ] Seed-source strategy is accepted.
- [ ] Map requirement is accepted or rejected.
- [ ] Evidence-photo policy is accepted or deferred.
- [ ] MVP scope is updated.
- [ ] Relevant ADRs are added or superseded.

---

## Issue 7 — Produce the build-ready project plan

**Type:** Planning

### Objective

Create the PRD, UX flows, architecture, schema, security baseline, test plan, and ordered implementation backlog.

### Acceptance criteria

- [ ] Product Requirements Document completed.
- [ ] MVP scope frozen.
- [ ] User flows and wireframes completed.
- [ ] Data model and data dictionary completed.
- [ ] Verification and moderation policy finalized.
- [ ] Technical architecture accepted.
- [ ] Security/privacy baseline accepted.
- [ ] Test strategy completed.
- [ ] Implementation issues ordered by dependency.
- [ ] Pilot success and pause criteria defined.
