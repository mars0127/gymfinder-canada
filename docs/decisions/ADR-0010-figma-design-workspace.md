# ADR-0010: Figma as the Visual Design and Handoff Workspace

- **Status:** Accepted
- **Date:** 2026-08-19

## Context

The product requires search, filtering, comparisons, gym profiles, verification states, and correction flows. These interactions need a shared visual workspace before frontend implementation. The product owner has access to a Figma Education subscription.

## Decision

Use Figma for:

- information architecture;
- user flows;
- low-fidelity wireframes;
- design foundations and variables;
- reusable components;
- responsive high-fidelity screens;
- clickable prototypes;
- developer-handoff annotations.

Truth boundaries are divided as follows:

- accepted decisions and the PRD control product scope and behavior;
- Figma controls approved visual intent and interaction presentation;
- schema and architecture documents control data and system semantics;
- tested production code controls actual runtime behavior.

Figma plan-specific features are optional. The project must not depend on a feature until its availability in the founders' account is verified.

## Consequences

- Material visual changes should be reflected in Figma or explicitly recorded as implementation divergence.
- Figma cannot override verification, privacy, security, or source-policy rules.
- Competitor products may be studied for patterns but their logos, artwork, copy, branding, and complete screen compositions may not be copied.
- Both Codex and Claude may use Figma context during implementation when configured and assigned.
