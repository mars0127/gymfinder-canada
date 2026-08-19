# Data Source Policy

## Objective

Build a traceable, maintainable gym-fact dataset without depending on prohibited scraping, copied reviews, unclear licences, or unstable commercial APIs.

## Core rule

A source may help discover a gym without becoming the canonical source of every fact about that gym.

Canonical GymFinder entities, source records, and verified facts should remain separate.

## Source hierarchy

### Preferred

1. **Direct founder observation** — recent, documented, and limited to observable facts.
2. **Gym-owned website** — discrete factual claims with page reference and retrieval date.
3. **Direct gym submission** — later, after staff authority is verified.
4. **Toronto Open Data** — municipal facilities and public programs under applicable licence terms.
5. **Permitted open place data** — used for discovery and entity resolution with attribution/licence tracking.
6. **Accepted community contribution** — structured fact, observation date, and moderation history.

### Conditional

- Official gym social-media posts containing a discrete current facility fact.
- OpenStreetMap records, subject to attribution and database-licensing architecture.
- Overture Places records, subject to source-specific attribution and quality audit.
- User-submitted evidence images, subject to privacy, copyright, moderation, and file-safety controls.
- Direct phone or email confirmation, recorded as a dated source note.

### Prohibited for the MVP dataset

- Google Maps scraping.
- Copied Google reviews or photos.
- Reddit API ingestion or scraped Reddit content.
- Automated extraction that publishes facts without human review.
- AI-generated or inferred equipment data.
- Photos copied from a gym website without permission or a valid licence.
- Personal information about gym patrons or individual staff beyond necessary public business contacts.

## Fact record requirements

Every important fact should be able to retain:

```text
canonical_gym_id
attribute_or_equipment_type
value
source_type
source_reference
source_licence_or_terms_note
observed_at
retrieved_at
submitted_by
verification_status
reviewed_by
reviewed_at
expires_or_recheck_at
conflict_status
```

Not every field must be displayed publicly, but it must be available for audit where relevant.

## Research evidence versus product data

Public discussions may be reviewed to understand user problems and vocabulary. They must not be silently converted into durable gym facts.

Example:

- Permitted research conclusion: “Users repeatedly ask whether gyms have a pendulum squat.”
- Not permitted product fact: “Gym X has a pendulum squat because an anonymous comment said so.”

## Automated collection rule

Before automating collection from any website or API:

1. Review the official terms and robots instructions.
2. Define exactly which discrete facts are needed.
3. Define retention and deletion obligations.
4. Record attribution requirements.
5. Add rate limiting and caching where permitted.
6. Keep results in a review queue.
7. Confirm the product remains functional if the source disappears.

## Images

The initial preference is to avoid a public image gallery. Evidence images, if enabled, should be limited, moderated, stripped of metadata, and focused on equipment rather than identifiable people.
