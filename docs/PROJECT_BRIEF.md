# Project Brief

## Working title

**GymFinder Canada**

The name is provisional. The initial product scope is Toronto, not Canada-wide coverage.

## Project status

**PLANNING**

Production implementation is not authorized until the build-ready planning package is accepted.

## Problem

Gym seekers can usually find addresses, general reviews, and basic hours, but often cannot reliably determine whether a specific gym location has the exact equipment, machine manufacturers, facilities, access rules, or services required for their training.

The information that does exist is fragmented across:

- official gym websites;
- public facility datasets;
- photographs;
- mapping platforms;
- social media;
- community discussions;
- direct experience inside the facility.

It is frequently incomplete, location-insensitive, stale, or difficult to compare.

## Product hypothesis

A Toronto-focused product can help strength-training users make better gym decisions by presenting structured, comparable gym facts with visible provenance, observation dates, and verification status.

This remains a product hypothesis until later pilot evidence is available.

The central loop is:

```text
research or import a fact
        ↓
user searches and compares
        ↓
user visits or recognizes a gym
        ↓
user confirms or corrects one fact
        ↓
submission is reviewed
        ↓
confidence and freshness improve
```

## Primary initial user

A Toronto strength-training user who cares about one or more exact requirements, such as:

- particular machine types;
- equipment manufacturers;
- rack or platform availability;
- dumbbell maximum weight;
- turf and sled space;
- day passes or access terms;
- sauna, pool, showers, or parking;
- women-only or private facilities;
- accessibility features.

This includes bodybuilders, powerlifters, hypertrophy-focused lifters, and serious recreational strength trainees. The product may broaden later after evidence supports doing so.

## Value proposition

> Find a Toronto gym that fits how you actually train, and understand why each result matches.

The product should answer questions such as:

- Which nearby gyms have a pendulum squat?
- Which locations have Prime or Atlantis equipment?
- Which gyms offer both several racks and a day pass?
- Which gym meets four of five requirements, and which requirement is missing or unknown?
- When was a fact last observed, and what evidence supports it?

## Product principles

### 1. Depth before breadth

Thirty complete profiles are more useful than thousands of empty shells.

### 2. Unknown is not no

Missing information remains `unknown`; it cannot silently become `absent`.

### 3. Facts before opinions

The MVP focuses on structured facility facts rather than open-ended ratings or reviews.

### 4. Evidence before confidence

Every important fact should retain its source, observation date, and verification state.

### 5. Transparent matching

Results must explain which requirements matched, failed, or remain unknown. Avoid unexplained AI-generated scores.

### 6. Human-reviewable changes

Crowdsourced submissions propose changes; they do not immediately overwrite approved data.

### 7. Privacy and accessibility by design

Do not store unnecessary location histories or identities. The list experience must remain usable without relying on a map.

### 8. Near-zero-cost MVP

Avoid paid infrastructure or commercial data dependencies until real usage justifies them.

### 9. Pattern-informed, independently designed

Use comparable products to learn interaction patterns, but create GymFinder's own product decisions, visual system, copy, and implementation.

## Provisional MVP outcome

A mobile-friendly website containing approximately 30–50 deeply profiled Toronto gyms where users can:

- search by location or area;
- set must-have and preferred requirements;
- filter by equipment, manufacturer, amenities, access, and services;
- understand why each gym matched;
- compare two or three gyms;
- see source, freshness, and verification indicators;
- submit a structured confirmation or correction.

## Explicit non-goals

The MVP is not:

- a Canada-wide directory;
- a general review platform;
- a class-booking marketplace;
- a social network;
- a personal-trainer marketplace;
- a payment or membership-purchase system;
- a real-time crowding system;
- an AI-generated gym-fact system;
- a native mobile application;
- dependent on gym-operator participation.

## Build-ready planning inputs

Before production implementation is authorized, the founders will accept:

1. competitor UX pattern audit;
2. PRD v1;
3. Figma information architecture, flows, design baseline, and handoff;
4. five-gym data-feasibility calibration;
5. data model and equipment taxonomy;
6. technical architecture, security/privacy baseline, and test strategy;
7. dependency-ordered implementation backlog;
8. planning closeout and explicit implementation decision.

External user interviews, surveys, usability tests, gym partnerships, and operator contact are not required for the initial build-ready plan. They may be reconsidered after a prototype or alpha produces concrete questions.
