# Planning Evidence and Validation Plan

## Purpose

The current objective is not to perform ceremonial customer discovery. It is to reduce specific planning risks quickly enough to produce a build-ready product, design, data, and architecture plan.

Before an evidence activity begins, complete:

> We are uncertain about **[decision]**. We will gather **[evidence]**. We will choose **[option]** using **[decision rule]**.

Do not conduct an activity that cannot change a decision.

## Current evidence streams

| Uncertainty | Current evidence | Decision rule | Required before implementation? |
|---|---|---|---|
| Which discovery and comparison patterns should GymFinder use? | Competitor UX pattern audit plus founder product judgment and accessibility heuristics. | Adopt or adapt patterns that support the accepted jobs without copying proprietary design. | Yes |
| Can candidate gym facts be obtained and maintained responsibly? | Five-gym data-feasibility calibration. | Keep required fields only when they have a credible source and maintenance path; retain unknown where necessary. | Yes |
| Which attributes belong in P0? | Competitor patterns, product requirements, calibration results, and founder priorities. | Include attributes that materially support the primary job and can be represented honestly. | Yes |
| Can the model represent uncertainty, provenance, corrections, and conflicts? | Data-model design with fixtures; bounded spike only if required. | Authorize implementation only when these states remain distinct and queryable. | Yes |
| Is an interactive map required at launch? | Competitor patterns, Figma flows, list-first design, accessibility, and cost analysis. | Include only when it materially improves the critical path and fits the near-zero-cost plan. | Yes |
| Are users willing to contribute at scale? | Future alpha and beta behavior. | Do not add complex incentives until actual contribution behavior is observed. | No |
| Are gym operators willing to claim profiles or offer trials? | Future outreach after a credible product exists. | Inform later business features only. | No |

## External user testing

External interviews, surveys, and usability tests are deferred until a prototype or functional alpha. They are not part of the current build-ready planning gate.

This choice accelerates planning but leaves some assumptions unproven. The PRD and planning closeout must identify those assumptions, and the pilot must measure real search, comparison, profile, and correction behavior.

A founder may reopen one targeted test earlier only when a named product or accessibility decision cannot be resolved through existing evidence.

## Competitor-pattern protocol

Use direct and adjacent products as pattern evidence, not as product-data sources or designs to copy.

For each product:

- record the product, platform, source, and retrieval date;
- inspect the relevant flow rather than only marketing pages;
- identify the user problem addressed;
- describe the interaction and information pattern in neutral terms;
- record strengths, weaknesses, and accessibility concerns;
- choose `adopt`, `adapt`, `reject`, or `defer`;
- explain the GymFinder-specific decision.

Do not copy:

- logos or brand colours as identity;
- proprietary artwork or photos;
- marketing copy;
- user reviews or private content;
- a complete page composition;
- restricted product data.

Store sanitized notes under `research/competitor-patterns/` and synthesize them in `docs/COMPETITOR_UX_PATTERN_AUDIT.md`.

## Five-gym data-calibration protocol

Use five varied Toronto facilities:

1. major chain;
2. budget chain;
3. independent strength/bodybuilding gym;
4. municipal fitness centre;
5. premium or multi-amenity gym.

Attempt only candidate P0 fields first. For every fact:

- preserve source type and reference;
- distinguish observation date from retrieval date;
- use present, absent, or unknown;
- never infer absence from silence;
- record contradictions;
- record collection and maintenance difficulty;
- identify whether operator contact would be needed, without making contact a requirement.

Suggested outputs:

- five calibration records;
- attribute-completeness matrix;
- source comparison;
- contradiction and duplicate notes;
- recommended required, optional, and deferred fields;
- provisional canonical-source strategy;
- maintenance implications.

This is a planning calibration, not a statistical audit or demand test. Expand the sample only when the first five do not cover enough source or facility variation.

## Official technical research

Mutable claims about frameworks, Figma features, APIs, free tiers, mapping services, Supabase, hosting, privacy rules, or platform terms must be verified through current primary sources before they become architecture assumptions.

Record:

- exact claim;
- official source;
- publication or update date when available;
- retrieval date;
- implication;
- uncertainty or expiry trigger.

## Technical spikes

Use a spike only when a material planning decision cannot be answered through documentation, fixtures, or a small model.

A spike issue must define:

- question being tested;
- scope and time boundary;
- fixture-only or remote-service permissions;
- promotion or disposal criteria;
- acceptance evidence;
- explicit non-goals.

A spike is not permission to scaffold the production product.

## Later live-product evidence

After an alpha or beta exists, stronger evidence includes:

- search completion;
- zero-result and unknown-result searches;
- filters used;
- gym comparisons;
- profile views;
- outbound clicks;
- accepted corrections;
- stale facts reconfirmed;
- abandoned flows;
- accessibility findings;
- operator claim requests.

These observations should drive later UX, incentive, and expansion decisions.

## Privacy and source handling

- Do not commit participant identities, contact details, recordings, or precise private locations.
- Do not copy restricted platform content into the repository or product dataset.
- Do not store screenshots that expose private accounts or personal data.
- Separate research evidence from product data.
- Respect source attribution, licence, and deletion requirements.

## Stop rules

Stop or narrow an evidence activity when:

- the decision is already clear;
- new observations no longer change the decision;
- the method cannot produce reliable evidence;
- the cost exceeds the importance of the decision;
- it requires prohibited or unstable data access;
- it begins turning workflow research into the product.
