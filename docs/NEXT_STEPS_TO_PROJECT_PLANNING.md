# Next Steps to Formal Project Planning

This is the shortest responsible path from the current repository to a build-ready project plan.

## Principle

Do not perform research because startup processes say that research should occur. Every activity must answer a decision that would otherwise remain uncertain.

Gym-operator outreach is not on the critical path. Formal interviews are not on the critical path.

## Step 1 — Founders align on the repository decisions

Both founders review:

- `PROJECT_BRIEF.md`;
- `MVP_SCOPE.md`;
- `DECISIONS.md`;
- `SOURCE_POLICY.md`;
- `VERIFICATION_POLICY.md`.

Any disagreement becomes a comment on the first alignment issue. Resolve it through a decision update, not through separate AI chats.

**Output:** accepted provisional brief and assigned research ownership.

## Step 2 — Run a fast ten-gym data audit

Choose ten deliberately varied Toronto facilities:

- chain locations;
- independent strength/bodybuilding gyms;
- municipal facilities;
- one or two locations with poor public information.

For each location, attempt to resolve the P0 fields in `ATTRIBUTE_DICTIONARY.md` and record:

- value;
- source;
- observation/retrieval date;
- confidence;
- time or difficulty;
- conflicts;
- whether direct contact would be required.

Start with ten, not twenty. Expand to twenty only when the first ten produce contradictory results or do not cover enough facility types.

**Decision unlocked:** whether the data is obtainable and which attributes belong in the MVP.

## Step 3 — Test the selection task, not enthusiasm for the idea

Do not conduct generic interviews asking whether people “would use” the product.

Use the cheapest credible evidence available, in this order:

1. Each founder independently reconstructs a recent or realistic gym-selection task and documents missing information.
2. Review public discussions to identify recurring decision criteria; use them as research evidence only, not as product data.
3. Ask three to five accessible gym users to complete an actual comparison task using the audited profiles or a simple mock-up.
4. Conduct a focused conversation only when a specific unresolved decision remains.

A useful task test asks the participant to choose among gyms under real constraints and explain what information changed the decision. It does not ask for a favourable opinion of the concept.

**Decision unlocked:** which filters and comparisons are decision-critical.

## Step 4 — Create a narrow data-model spike

The spike must prove that the system can represent:

- canonical gyms and source records separately;
- equipment types, manufacturers, models, and quantities;
- `present`, `absent`, and `unknown`;
- provenance and observation dates;
- proposed corrections without overwriting approved facts;
- conflicts and verification events;
- must-have matching with an explanation of unmet requirements.

The spike does not need final UI, production authentication, rewards, payments, or a staff dashboard.

**Decision unlocked:** whether the provisional stack and schema can support the product correctly.

## Step 5 — Freeze planning decisions

Use the evidence from Steps 2–4 to resolve the open decisions in `DECISIONS.md`:

- seed source;
- Toronto seed area;
- P0 attributes;
- equipment taxonomy depth;
- completeness threshold;
- map requirement;
- evidence-photo policy;
- authentication timing;
- final MVP boundaries.

Anything not resolved is explicitly deferred.

## Step 6 — Produce the formal planning package

The build-ready plan will contain:

1. Product Requirements Document.
2. Frozen MVP scope.
3. User flows and low-fidelity wireframes.
4. Data model and data dictionary.
5. Verification and moderation policy.
6. Technical architecture.
7. Security and privacy baseline.
8. Test strategy.
9. Ordered implementation backlog with acceptance criteria.
10. Pilot launch and measurement plan.

## Planning-readiness gate

Formal planning can be finalized when all of the following are true:

- [ ] Both founders accept the project brief and MVP boundaries.
- [ ] A ten-gym audit has tested the proposed source and attribute model.
- [ ] The founders can identify the high-value attributes that are realistically maintainable.
- [ ] At least one real or realistic gym-selection task has been completed using the structured data.
- [ ] Additional task tests have been performed only where uncertainty required them.
- [ ] The data-model spike represents provenance, uncertainty, corrections, and conflicts.
- [ ] Open decisions affecting architecture are accepted or explicitly deferred.
- [ ] Gym-operator participation is not assumed in any critical path.

## Explicitly unnecessary before planning

- gym partnerships;
- operator interviews;
- a survey with a large sample;
- payment validation;
- a logo or final name;
- a domain;
- 50 completed gym profiles;
- Canada-wide market research;
- production deployment.
