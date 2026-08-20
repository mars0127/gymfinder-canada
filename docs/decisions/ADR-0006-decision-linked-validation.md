# ADR-0006: Validation Must Be Decision-Linked

- **Status:** Accepted; current preplanning evidence sequence refined by ADR-0011
- **Date:** 2026-08-19

## Context

Interviews, surveys, and other research can become formalities that collect polite opinions without changing the product. The founders have limited participant and operator access and want to reach a build-ready plan quickly.

## Decision

No interview, survey, or testing quota will be imposed. Every evidence activity must name:

- the uncertain decision;
- the evidence sought;
- the rule for interpreting it;
- the action that follows.

For the current planning stage, use founder direction, competitor-pattern evidence, five-gym data calibration, current primary technical sources, Figma design reasoning, and bounded technical spikes where necessary. External user interviews and usability tests are deferred under ADR-0011 unless a founder explicitly reopens a named question.

## Consequences

- Faster path to a build-ready plan.
- Less performative research.
- Assumptions not validated by live use must be stated explicitly.
- Prototype, alpha, and pilot behavior become important later evidence.
- New evidence may reopen the smallest affected decision without restarting the entire planning process.
