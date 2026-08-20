# Provisional MVP Scope

**Status:** Provisional until the build-ready planning closeout.

## MVP objective

Create a Toronto gym-discovery and comparison product whose pilot can test whether structured, current, and visibly sourced gym information improves real gym decisions.

The objective is not to prove that a large map can be populated.

## Included

### Public discovery

- Search by neighbourhood, postal code, or approximate location.
- Optional distance preference.
- Must-have and preferred requirements.
- List-first results.
- Optional map only if planning confirms that it improves the critical path without disproportionate cost or accessibility burden.

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
- Explanation of matched, unmet, and unknown requirements.
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

- Canada-wide or Ontario-wide public coverage.
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
- the accepted majority of P0 attributes resolved;
- at least one traceable source for each displayed P0 fact;
- an observation or retrieval date;
- no unresolved critical duplicate or closure conflict.

The exact threshold will be decided after the five-gym calibration.

## Scope-change rule

A proposed addition belongs in the MVP only when all of the following are true:

1. It directly supports the MVP objective.
2. It is supported by accepted product requirements, founder judgment, competitor-pattern evidence, later product evidence, or a material accessibility/safety need.
3. The required data can be obtained and maintained responsibly.
4. It does not create disproportionate moderation, privacy, security, accessibility, or cost burden.
5. The decision is recorded in `DECISIONS.md`.
