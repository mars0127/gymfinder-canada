# ADR-0007: Provisional Next.js and Supabase Stack

- **Status:** Provisional
- **Date:** 2026-08-19

## Context

The product requires public indexable pages, relational data, authentication for contributors, fact-level provenance, moderation, and server/database authorization. The founders also require a near-zero-cost MVP.

## Decision

Use TypeScript with Next.js for the web application and Supabase Postgres/Auth/Storage for the provisional architecture, subject to a data-model and security spike.

## Alternatives considered

- Streamlit, SQLite, and Python.
- Firebase.
- Fully custom backend and database.
- Static site with manually generated profiles.

## Consequences

- The team must understand Next.js server/client boundaries and Supabase Row Level Security.
- A relational schema fits facts, sources, equipment, and verification events.
- Managed authentication reduces the need to build password storage.
- The decision remains reversible before implementation begins.

## Validation

The spike must prove authorization boundaries, fact history, filtering, and free-tier suitability before this ADR becomes accepted.
