# Candidate Attribute Dictionary

**Status:** Candidate set for the five-gym planning calibration. This is not the final database schema or final public filter list.

## Data-state rule

Presence-like attributes require three states:

- `present` — affirmative evidence exists;
- `absent` — affirmative evidence supports absence;
- `unknown` — insufficient evidence.

Missing data must default to `unknown`, never `absent`.

## Priority definitions

- **P0:** candidate requirement for a launch-ready profile.
- **P1:** valuable when obtainable; may be incomplete.
- **P2:** later-phase or specialized.

## Gym identity

| Attribute | Priority | Intended type | Notes |
|---|---:|---|---|
| Canonical gym name | P0 | Text | GymFinder-controlled canonical value. |
| Source names and aliases | P0 | Related records | Preserve rebrands and source variants. |
| Operating status | P0 | Enum | Open, temporarily closed, permanently closed, unknown. |
| Address | P0 | Structured address | Do not treat map text as independently verified. |
| Neighbourhood | P0 | Controlled text | Useful for list-first discovery. |
| Coordinates | P0 | Geography | Source and precision must be recorded. |
| Website | P0 | URL | Official source when known. |
| Public phone | P1 | Text | Business contact only. |
| Gym type | P0 | Controlled enum | Chain, independent strength, municipal, community, other. |
| Chain or brand | P1 | Related entity | Location-level facts remain separate. |

## Access and pricing

| Attribute | Priority | Intended type | Notes |
|---|---:|---|---|
| Operating hours | P0 | Weekly schedule | Store source and observed/retrieved date. |
| Staffed hours | P1 | Weekly schedule | Distinct from member access. |
| 24/7 access | P0 | Tri-state | May depend on membership tier. |
| Open-gym access | P0 | Tri-state | Distinguish from class-only access. |
| Day pass | P0 | Structured offer | Status, price if known, eligibility, expiry/check date. |
| Free trial | P1 | Structured offer | Do not label free without material terms. |
| Price band | P0 | Enum | Prefer broad range in MVP over fragile exact pricing. |
| Contract requirement | P1 | Structured terms | Avoid legal interpretation; state published terms only. |

## Equipment representation

Do not create one permanent boolean column for every machine. Use related equipment records:

```text
equipment_type
manufacturer
model
loading_type
quantity
presence_state
notes
observed_at
verification_status
```

### Candidate equipment types

| Equipment type | Priority | Additional detail |
|---|---:|---|
| Power rack | P0 | Quantity. |
| Squat rack / half rack | P0 | Quantity. |
| Lifting platform | P0 | Quantity. |
| Dumbbells | P0 | Maximum weight when known. |
| Hack squat | P0 | Manufacturer/model when known. |
| Pendulum squat | P0 | Manufacturer/model when known. |
| Leg press | P0 | Type and manufacturer when known. |
| Smith machine | P0 | Quantity; angled/vertical later. |
| Cable station | P0 | Quantity or station type. |
| Belt squat | P1 | Manufacturer/model when known. |
| Chest-supported row | P1 | Plate-loaded or selectorized. |
| Plate-loaded chest press | P1 | Manufacturer/model when known. |
| Plate-loaded shoulder press | P1 | Manufacturer/model when known. |
| Plate-loaded row | P1 | Manufacturer/model when known. |
| Specialty barbells | P1 | Safety squat, trap, Swiss, deadlift, other. |
| Bumper plates | P1 | Presence and approximate availability. |
| Calibrated plates | P2 | Powerlifting-specific. |
| Combo rack | P2 | Powerlifting-specific. |
| Glute-ham developer | P2 | Specialized. |
| Reverse hyper | P2 | Specialized. |
| Hip-thrust machine | P2 | Specialized. |
| Stair climber | P1 | Quantity later if useful. |
| Treadmills | P1 | Quantity later if useful. |

### Manufacturer

Manufacturer is a related entity, not uncontrolled free text where avoidable. Preserve aliases and spelling variants.

Candidate examples for taxonomy testing include:

- Atlantis;
- Prime Fitness;
- Panatta;
- Gymleco;
- Arsenal Strength;
- Hammer Strength;
- Life Fitness;
- Technogym;
- Matrix;
- Precor;
- Rogue;
- Eleiko;
- Watson;
- Cybex.

This list is illustrative, not a claim about any gym.

## Amenities and facilities

| Attribute | Priority | Intended type | Notes |
|---|---:|---|---|
| Showers | P0 | Tri-state | Operational availability may differ from physical presence. |
| Lockers | P1 | Tri-state/details | Day-use versus rental later. |
| Sauna | P0 | Tri-state | Note closures or access restrictions. |
| Steam room | P1 | Tri-state | Separate from sauna. |
| Pool | P1 | Tri-state | Access may depend on membership. |
| Turf | P0 | Tri-state/details | Size can remain descriptive initially. |
| Sled availability | P1 | Tri-state | Often depends on usable turf. |
| Parking | P0 | Structured | Free, paid, limited, unknown. |
| Towel service | P1 | Tri-state/details | May require a tier or fee. |
| Childcare | P1 | Tri-state/details | Hours and age restrictions later. |
| Women-only facility | P1 | Tri-state | Factual facility attribute. |
| Women-only area or hours | P1 | Structured | Preserve schedule/details. |
| Private changing space | P1 | Tri-state | Do not infer from generic washrooms. |
| Accessible entrance | P0 | Tri-state | Prefer direct or authoritative evidence. |
| Accessible washroom | P1 | Tri-state | Do not infer from entrance accessibility. |
| Elevator access | P1 | Tri-state | Relevant for multi-level facilities. |

## Programs and services

| Attribute | Priority | Intended type | Notes |
|---|---:|---|---|
| Personal training | P1 | Tri-state/details | Availability, not trainer quality. |
| Strength coaching | P1 | Tri-state/details | Powerlifting/bodybuilding where stated. |
| Group classes | P2 | Tri-state | Detailed schedules are outside MVP. |
| Rehabilitation services | P2 | Tri-state/details | Avoid medical-quality claims. |

## Excluded subjective labels

Do not initially model these as verified facts:

- safe;
- welcoming;
- intimidating;
- hardcore;
- beginner-friendly;
- clean;
- good atmosphere;
- inclusive;
- crowded in real time.

They may later require carefully defined observation methods, sufficient samples, and moderation.
