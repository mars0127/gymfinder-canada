# AI Agent Workflow

## Purpose

This document defines how the founders use ChatGPT, Codex, Claude Code, Figma, and GitHub without turning model names into permanent job titles or allowing chat context to replace repository truth.

The project-specific control loop is:

```text
Founder intent
    ↓
ChatGPT/Codex planning and supervision
    ↓
Bounded issue or task contract
    ↓
Assigned agent work
    ↓
Repository or Figma artifact
    ↓
Proportional evidence
    ↓
Independent challenge when valuable
    ↓
Human acceptance
    ↓
Decision, closeout, and workflow learning
```

## 1. Authority and stages

### Human founders

The founders decide:

- the problem and product value;
- scope and priorities;
- acceptable risk;
- major trade-offs;
- whether evidence is sufficient;
- what merges and ships.

### Planning control layer — current stage

During `PLANNING`, ChatGPT and/or Codex may:

- conduct and synthesize research;
- structure product decisions;
- draft the PRD;
- design information architecture and Figma work plans;
- propose data and technical architecture;
- create bounded agent contracts;
- reconcile outputs;
- maintain continuity and the recovery capsule.

Under the current owner decision, Claude is not part of the default planning workflow and enters when implementation is authorized. That decision may be superseded later through the decision log.

### Implementation agents — later stage

After explicit implementation authorization, Codex and Claude are peer agents. Either may own:

- repository research;
- design implementation;
- frontend or backend work;
- database and migrations;
- authentication and authorization;
- tests;
- debugging;
- documentation;
- security analysis;
- independent review.

No permanent model specialization is binding.

## 2. Agent assignment

Choose the agent per issue using:

- existing relevant context;
- tool and integration access;
- terminal, browser, Figma, or worktree needs;
- independence from prior reasoning;
- context-transfer cost;
- current usage availability;
- measured GymFinder performance on similar tasks;
- task risk and blast radius.

Record the assignment in the issue. Do not generalize a few successes into a permanent claim that one model is universally superior.

## 3. Working modes

### Mode A — Single-agent ownership

One agent owns a bounded issue from inspection through report-back.

Use for ordinary planning artifacts, isolated components, scripts, documentation, and low-risk fixes.

### Mode B — Parallel plan comparison

Two agents independently propose options before implementation. A founder or supervising AI selects or combines the result.

Use for difficult-to-reverse architecture, schema, security, or major UX decisions.

Do not build two complete implementations merely to compare opinions unless the expected value justifies the cost.

### Mode C — Parallel implementation against a frozen interface

Two agents implement separable workstreams using an accepted contract.

Example:

```text
Shared contract: SearchCriteria → ExplainedGymMatch[]
Codex: matching and explanation engine
Claude: data-access layer and representative fixtures
```

Do not parallelize a serial dependency whose upstream assumptions are unstable.

### Mode D — Risk-triggered independent review

One agent implements. Another agent, preferably in a sufficiently independent context, derives the diff and evidence independently.

Use for high-risk boundaries listed in `AGENTS.md`.

### Mode E — Same-agent correction

The implementing agent normally fixes routine defects while context is fresh. Use another agent when the diagnosis is disputed, the first agent is stuck, or independent interpretation has real value.

## 4. Issue contract

Every consequential issue should answer:

- What outcome must become true?
- What is binding?
- What is current evidence or hypothesis?
- What evidence will prove acceptance?
- What is explicitly excluded?
- What implementation freedom exists?
- Which remote or destructive actions are allowed?
- Does the work require independent review?

Use `docs/templates/AGENT_TASK_CONTRACT.md` when a detailed contract is warranted.

## 5. Context selection

### Reuse an existing context when

- the role continues;
- prior reasoning remains relevant;
- the task is a direct correction;
- reconstruction cost is high and independence is unnecessary.

Use a delta update rather than repeating all history.

### Use a fresh context when

- the role changes;
- independent review matters;
- a clean architecture boundary is reached;
- old plans may bias the decision;
- context debt has accumulated;
- cold-start repository recovery should be tested.

## 6. Git and work isolation

For consequential work:

1. verify repository root, branch, HEAD, and working state;
2. stop on a material mismatch;
3. use one branch or worktree per issue;
4. do not let two agents edit the same branch simultaneously;
5. do not reset, stash, clean, switch, or repair history without authority;
6. do not push, open a PR, merge, deploy, mutate hosted services, alter secrets, or add dependencies without explicit permission.

## 7. Figma integration

Figma is used for visual product artifacts. Either agent may use Figma context when assigned and configured.

Before frontend implementation:

- identify the approved Figma frame or component;
- identify the linked requirement;
- confirm responsive and state coverage;
- identify reusable code components;
- record material divergence rather than silently improvising.

Figma is not authoritative for data semantics, authorization, or product scope.

## 8. Evidence and acceptance

Use evidence proportional to the risk:

```text
focused tests
    → contract or schema checks
    → architecture/security checks
    → full suite
    → build/type/lint
    → browser, device, accessibility, or deployment evidence when required
```

Tests prove only the property they actually observe. Reports must state limitations explicitly.

## 9. Independent review triggers

Strong triggers include:

- authentication, authorization, and RLS;
- sensitive user or location data;
- immutable fact history and correction semantics;
- public mutations and moderation;
- foundational cross-layer contracts;
- significant dependencies or security changes;
- consequential concurrency;
- large or hard-to-observe implementations.

A review finding requires a concrete violated invariant, reachable failure, or evidence defect. Review must not invent unrelated hardening.

Use `docs/templates/INDEPENDENT_REVIEW_CONTRACT.md`.

## 10. Failure classification

Before changing production code, classify a failure:

- production defect;
- test defect;
- wrong observation boundary;
- tool or environment failure;
- nondeterminism;
- stale expectation;
- specification or architecture conflict;
- missing input;
- stale external assumption;
- review-scope creep.

Fix the smallest wrong layer. Do not weaken a correct test merely to make the suite green.

## 11. Report-back

A consequential run reports:

- identity and starting checkpoint;
- outcome and files changed;
- architecture, data, security, Figma, dependency, and remote effects;
- focused and broader evidence;
- failures and corrections;
- scope and forbidden-change audit;
- final Git and service state;
- remaining uncertainty;
- recommended next action;
- exact status.

Use `docs/templates/AGENT_RUN_REPORT.md`.

No invisible chaining: when a task says return the report and wait, the next governed action begins only after the report is reviewed.

## 12. Status language

Use exact states:

- `PLANNING`
- `IMPLEMENTATION AUTHORIZED`
- `IMPLEMENTED — REVIEW PENDING`
- `CORRECTION REQUIRED`
- `TECHNICALLY ACCEPTED — MANUAL EVIDENCE PENDING`
- `CLOSED`
- `BLOCKED`

Do not use “done” when required evidence, review, or approval remains.

## 13. Workflow learning without drag

Track only when useful:

- first-pass acceptance;
- review findings and severity;
- correction cycles;
- scope violations;
- human steering;
- context reconstruction failures;
- rework;
- agent/tool performance by task category.

Promote repeated lessons into repository guidance or tests. Do not build elaborate orchestration infrastructure before repeated friction earns it.

If several runs occur without closing a meaningful boundary, reassess whether tasks are too small, prompts are too prescriptive, review is repetitive, or assumptions remain unstable.
