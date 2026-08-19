# Verification and Correction Policy

## Objective

Communicate what is known, how it is known, and how recently it was observed without implying more certainty than the evidence supports.

## Verification applies to facts, not entire gyms

A profile can contain a mixture of:

- official website facts;
- founder observations;
- community reports;
- unresolved conflicts;
- unknown fields.

A single profile-level checkmark must not imply that every field is current and accurate.

## Public statuses

| Status | Meaning |
|---|---|
| Imported — unverified | Added from an allowed seed source but not independently confirmed. |
| Public-source confirmed | Supported by a current permitted primary/public source. |
| Community reported | Submitted by one contributor and awaiting stronger confirmation. |
| Community confirmed | Supported by multiple sufficiently independent accepted observations or strong evidence. |
| Founder verified | Recently observed by a founder or authorized moderator. |
| Staff confirmed | Confirmed by an authenticated gym representative. This is not the same as independent verification. |
| Disputed | Credible sources conflict. |
| Stale | The fact has exceeded its recheck interval. |
| Unknown | Insufficient information. |

## Internal evidence fields

Each fact or verification event should support:

- source type;
- source reference;
- contributor or system actor;
- observed date;
- submitted date;
- reviewed date;
- evidence attachment where permitted;
- confidence status;
- conflict status;
- recheck date;
- moderation notes.

## Contribution workflow

```text
user selects one fact
        ↓
confirms, denies, or proposes a value
        ↓
provides observation date and optional evidence
        ↓
server validates and rate-limits the submission
        ↓
submission enters pending review
        ↓
moderator approves, rejects, requests clarification, or marks disputed
        ↓
new verification event is appended
        ↓
current fact state is recalculated
```

Do not overwrite or delete the prior evidence history when a value changes.

## Independence and abuse

A raw confirmation count is not sufficient evidence by itself.

The system should eventually consider:

- account age and accepted history;
- whether contributors are distinct;
- repeated submissions from the same account;
- suspicious account or network patterns;
- evidence strength;
- recency;
- staff conflicts of interest;
- coordinated positive or negative manipulation.

Do not publicly expose a complicated trust score during the MVP. Use clear labels and dates.

## Conflicts

When credible sources conflict:

1. Preserve both source records.
2. Mark the fact disputed.
3. Avoid silently selecting the more favourable value.
4. Seek newer or stronger evidence.
5. Record the moderator decision and reasoning.

Example: a gym website lists a sauna, while recent contributors report that it is closed. The physical amenity may exist while operational availability is disputed. The model should be capable of representing both.

## Freshness

Recheck intervals are field-specific and provisional.

| Fact category | Candidate recheck interval |
|---|---:|
| Trial or promotion | 30 days or explicit expiry |
| Price and day-pass terms | 60–90 days |
| Operating and staffed hours | 60–90 days |
| Equipment presence and quantity | 6–12 months |
| Major amenities | 6–12 months |
| Accessibility facilities | 12 months or after a reported change |
| Address and operating status | Monitor whenever the profile is accessed or reviewed |

These intervals must be tested against actual change frequency and contribution volume.

## Rewards

The MVP does not provide financial rewards or trials for raw submissions.

Future recognition should reward accepted, accurate contributions rather than volume. Any material incentive connected to public content must be disclosed and cannot require a positive statement.

## Gym staff

Staff confirmation is useful but not automatically superior to all community evidence. Staff must not be able to erase accepted reports or change verification roles directly.

Staff-claim verification and permissions are deferred until operator participation becomes realistic.
