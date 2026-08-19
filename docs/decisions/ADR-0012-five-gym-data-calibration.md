# ADR-0012: Five-Gym Data-Feasibility Calibration During Planning

- **Status:** Accepted
- **Date:** 2026-08-19

## Context

The product depends on structured facts such as equipment presence, manufacturers, quantities, access rules, amenities, and freshness. Designing the schema and filter set only from imagined examples risks creating fields that cannot be populated or maintained. A ten- or twenty-gym audit would slow planning more than necessary.

## Decision

Run a five-gym data-feasibility calibration during planning using a varied Toronto sample:

1. major chain location;
2. budget chain location;
3. independent strength or bodybuilding gym;
4. municipal fitness centre;
5. premium or multi-amenity gym.

For candidate P0 facts, record:

- value;
- `present`, `absent`, or `unknown`;
- source and source type;
- observation or retrieval date;
- confidence;
- contradiction;
- collection and maintenance difficulty.

The calibration:

- requires no operator contact;
- is not customer validation;
- does not block the start of PRD or Figma work;
- must inform the final P0 fields, completeness threshold, source strategy, and schema before implementation authorization.

## Consequences

- Planning can proceed immediately in parallel with the calibration.
- Unknown results are useful and must not be converted into absence.
- The sample may be expanded only when the first five fail to expose enough source or facility variation.
