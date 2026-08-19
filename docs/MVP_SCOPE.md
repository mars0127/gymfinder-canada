# Provisional MVP Scope

**Status:** Provisional until the planning-readiness review.

## MVP objective

Prove that structured, current, and visibly sourced gym information helps Toronto strength-training users choose between real gym locations more effectively than their current fragmented search process.

The objective is not to prove that a large map can be populated.

## Included

### Public discovery

- Search by neighbourhood, postal code, or approximate location.
- Optional distance preference.
- Must-have and nice-to-have requirements.
- List-first results.
- Optional map only if it does not compromise cost or usability.

### Gym profiles

- Name, address, neighbourhood, website, and gym type.
- Operating and access information where available.
- Structured equipment records.
- Equipment manufacturer when known.
- Selected amenities, facilities, and services.
- Source, observed date, and verification state for important facts.
- Clear distinction between present, absent, and unknown.

### Matching and comparison

- Deterministic filtering.
- Explanation of matched and unmet requirements.
- Comparison of two or three gyms using the same fields.

### Contributions

- Confirm one existing fact.
- Report an existing fact as incorrect.
- Propose a missing fact.
- State when the contributor observed it.
- Optionally attach limited evidence if the evidence policy permits it.
- Submissions enter review instead of directly altering approved facts.

### Administration

- A simple moderation workflow.
- Ability to approve, reject, or mark a submission as disputed.
- Audit history for approved changes.
- A custom staff dashboard is not required; database/admin tooling may be used initially.

## Excluded

- Canada-wide public coverage.
- Ontario-wide public coverage.
- Open-ended reviews or star ratings.
- Social feeds, chat, follows, or direct messages.
- Class schedules and booking.
- Personal-trainer marketplace.
- Payment processing or subscriptions.
- Automated trials, discounts, or contributor rewards.
- Paid placement or sponsored rankings.
- Real-time crowding.
- Daily streaks or complex gamification.
- Native iOS or Android applications.
- AI-generated gym facts.
- Reddit ingestion.
- Google Maps scraping or copied Google reviews/photos.
- Automatic publication of scraped data.
- Full gym-operator dashboard.
- Gym-operator participation as a launch dependency.

## Candidate profile-completeness requirement

A gym should not be treated as launch-ready merely because it has a name and location.

A provisional launch-ready profile should have:

- reliable identity and location;
- the majority of P0 attributes resolved;
- at least one traceable source for each displayed P0 fact;
- an observation or retrieval date;
- no unresolved critical duplicate or closure conflict.

The exact completeness threshold will be decided after the source audit.

## Scope-change rule

A proposed addition belongs in the MVP only when all of the following are true:

1. It directly supports the MVP objective.
2. There is evidence that the target user needs it for gym selection.
3. The required data can be obtained and maintained responsibly.
4. It does not create disproportionate moderation, privacy, security, or cost burden.
5. The decision is recorded in `DECISIONS.md`.
