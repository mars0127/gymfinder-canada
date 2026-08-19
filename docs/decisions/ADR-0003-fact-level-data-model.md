# ADR-0003: Verify Individual Facts, Not Entire Profiles

- **Status:** Accepted
- **Date:** 2026-08-19

## Context

A gym profile contains facts from different sources and dates. Staff may confirm hours while equipment remains community-reported. A single verified badge would overstate certainty.

## Decision

Store verification, provenance, observation date, conflict status, and freshness at the fact or verification-event level.

## Consequences

- The data model is more relational and complex.
- Public labels can be honest and specific.
- Corrections and disputes can preserve history.
- Matching can account for unknown or stale values.
