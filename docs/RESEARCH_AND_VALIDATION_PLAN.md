# Research and Validation Plan

## Purpose

Research exists to reduce a specific decision risk. It is not a ceremony, a credibility performance, or a requirement to collect a predetermined number of interviews.

Before any activity begins, complete this sentence:

> We are uncertain about **[decision]**. We will gather **[evidence]**. We will choose **[option A/B]** based on **[decision rule]**.

If the result cannot change a decision, do not conduct the activity.

## Current decision-linked research

| Uncertainty | Cheapest credible evidence | Decision rule | Required now? |
|---|---|---|---|
| Can core gym facts be obtained responsibly? | Ten-gym source and attribute audit. | Proceed when most P0 fields are obtainable with traceable, maintainable sources. | Yes |
| Which equipment and amenity filters matter? | Founder tasks, public problem evidence, then 3–5 task tests only if needed. | Keep attributes that materially alter a gym choice and can be maintained. | Yes, but no formal interview quota |
| Does the data model handle uncertainty and conflict? | Small technical spike with fixtures. | Proceed only when present/absent/unknown, provenance, corrections, and disputes remain distinct. | Yes |
| Are gym operators willing to claim or update profiles? | Future outreach after a credible sample profile exists. | Inform later staff features; does not block user MVP. | No |
| Will gyms offer trial codes? | Future partner experiment. | Build only after a gym voluntarily commits to a test. | No |
| Will users contribute at scale? | Observe beta behavior after users receive value. | Add incentives only after actual contribution rates are measured. | No |

## Evidence ladder

Use the least expensive level capable of resolving the uncertainty.

### Level 1 — Founder evidence

- Reconstruct a real past gym-search process.
- Attempt a new search with explicit constraints.
- Record what could and could not be determined.
- Compare independent founder conclusions.

This is not sufficient to prove broad demand, but it is sufficient to expose obvious assumptions and vocabulary problems.

### Level 2 — Existing behavioural evidence

Review public discussions, questions, and complaints to identify recurring decision criteria. Record:

- the user problem;
- what they attempted;
- which information was missing;
- whether exact equipment changed the decision.

Do not copy restricted content into the product database. Research evidence and product data are separate.

### Level 3 — Task-based test

Ask an accessible gym user to choose among real profiles under actual constraints.

Observe:

- which filters they use;
- which information they ignore;
- what they cannot understand;
- whether they can explain the final choice;
- whether they trust the verification labels.

This can be a short informal session. It is not a formal interview.

### Level 4 — Focused conversation

Use only when a decision remains unresolved after task evidence. Ask about past behavior, not hypothetical enthusiasm.

### Level 5 — Live product evidence

After a beta exists, usage and correction behavior become the strongest evidence:

- searches completed;
- profile views;
- comparisons;
- outbound clicks;
- accepted corrections;
- stale facts reconfirmed;
- failed searches caused by missing data.

## Ten-gym audit protocol

Select a mixed sample and record facts using `templates/GYM_PROFILE_AUDIT_TEMPLATE.md`.

For each fact:

- preserve the source type and reference;
- distinguish observation date from retrieval date;
- do not infer `no` from missing evidence;
- record contradictions;
- record the effort required;
- identify whether the value can be maintained without direct operator contact.

### Suggested success indicators

These are founder decision aids, not statistical claims:

- reliable identity and location for at least 8 of 10 gyms;
- approximately 80% resolution of the final candidate P0 fields across the sample;
- no dependence on prohibited sources;
- manageable duplicate and closure handling;
- a realistic path to maintaining 30–50 profiles.

## Task-test protocol

Use `templates/USER_TASK_TEST_TEMPLATE.md`.

A participant may use their own actual needs or a scenario such as:

> Choose a gym accessible from North York that has a pendulum squat, several racks, a day pass, and showers. Explain which requirement matters most and what information you still need.

Do not ask, “Would you use this app?” until after the task, and do not treat a positive answer as validation.

## Privacy

- Use participant codes, not names.
- Do not record precise home addresses.
- Do not commit emails or phone numbers.
- Do not record sensitive demographic information unless it is essential to a specific accessibility decision and the participant voluntarily provides it.
- Store any raw private notes outside the repository.

## Stop rules

Stop an activity when:

- the decision is already clear;
- new observations repeat existing evidence without changing the decision;
- the activity cannot produce reliable evidence;
- the cost exceeds the importance of the decision;
- it requires prohibited or unstable data access.
