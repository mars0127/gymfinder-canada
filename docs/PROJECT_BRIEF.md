# Project Brief

## Working title

**GymFinder Canada**

The name is provisional. The initial product scope is Toronto, not Canada-wide coverage.

## Project stage

Discovery and pre-planning.

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
- Which gym meets four of five requirements, and which requirement is missing?
- When was a fact last observed, and who or what supports it?

## Product principles

### 1. Depth before breadth

Thirty complete profiles are more useful than thousands of empty shells.

### 2. Unknown is not no

Missing information must remain `unknown`; it cannot silently become `absent`.

### 3. Facts before opinions

The MVP focuses on structured facility facts rather than open-ended ratings or reviews.

### 4. Evidence before confidence

Every important fact should retain its source, observation date, and verification state.

### 5. Transparent matching

Results must explain which requirements matched and which did not. Avoid unexplained AI-generated scores.

### 6. Human-reviewable changes

Crowdsourced submissions propose changes; they do not immediately overwrite approved data.

### 7. Privacy and accessibility by design

Do not store unnecessary location histories or participant identities. The list experience must remain usable without relying on a map.

### 8. Near-zero-cost validation

Avoid paid infrastructure or commercial data dependencies before the product demonstrates utility.

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

## Planning evidence required

Formal implementation planning can proceed after the founders have:

1. tested data acquisition on a small, varied Toronto gym sample;
2. identified a realistic high-value attribute set;
3. tested whether actual gym-choice tasks benefit from those attributes;
4. proven that the proposed data model can represent provenance, uncertainty, corrections, and conflicts.

Gym-operator interviews or partnerships are not required before planning.
