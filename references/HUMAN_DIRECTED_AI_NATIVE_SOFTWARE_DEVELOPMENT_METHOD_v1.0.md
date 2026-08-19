# Human-Directed AI-Native Software Development Method

**A practical operating system for prompting, governing, reviewing, and learning from AI software-engineering agents**

**Version 1.0 — 2026-08-19**

> Generalized from Project Atlas empirical evidence and current primary-source research on AI coding agents.

## Executive Summary

AI-assisted software development works best when prompt writing is treated as only one layer of a larger control system.

The transferable pattern is:

**Human authority → AI supervision/research → bounded coding agents → repository truth → mechanical verification → independent challenge when valuable → evidence-backed closeout → workflow learning.**

The central idea is not to micromanage every line of code. It is to make outcomes, boundaries, evidence, and recovery explicit enough that capable agents can work autonomously without silently redefining the product or overstating what has been proven.

This document generalizes lessons from Project Atlas and current agent-engineering research into a reusable method for other software projects. It is designed for a founder, product owner, engineer, student, or small team directing AI coding agents such as Codex, Claude Code, Copilot agents, or future equivalents.

The method has six priorities:

1. **Outcome before implementation.** Define what must become true and what must not change.
2. **Repository truth before memory.** The local repository and executable checks outrank chat recollection.
3. **Context engineering before prompt bloat.** Give agents the smallest high-signal context they need, and move durable knowledge into the repository.
4. **Evidence before acceptance.** Tests are evidence, not the entire truth. Match verification to the actual risk boundary.
5. **Independent review when its information value is high.** Do not review everything, but use genuinely independent agents for foundational, security, history, concurrency, and hard-to-observe boundaries.
6. **Learning without endless process.** Promote repeated lessons into the harness; do not let workflow optimization replace shipping.

Project Atlas supplied several empirical warnings. In one slice, 385 automated tests passed before an independent reviewer still found a Major cross-fact concurrency defect. In a later production slice, 461 tests and the full architecture suite passed before a fresh reviewer found three Major defects. A closed storage subphase later had to be narrowly reopened after downstream research exposed a historical time-zone compatibility flaw. These cases demonstrate why “green tests” and “closed” should mean “accepted under current evidence,” not “incapable of being challenged by new evidence.”

## 1. The Operating Model: Humans Direct, Agents Execute

A robust AI-native project separates **authority**, **reasoning/control**, **execution**, and **review**.

### 1.1 Human owner / product authority

The human owner decides:
- the problem worth solving;
- product value and priorities;
- scope;
- acceptable risk;
- major trade-offs;
- whether evidence is sufficient;
- what ships.

The human should not need to babysit every agent step. The goal is to spend human attention on decisions that actually require human judgment.

### 1.2 Supervising AI / engineering-control layer

A supervising AI can act as:
- product and architecture partner;
- researcher;
- security/privacy reviewer;
- agent allocator;
- prompt designer;
- evidence reviewer;
- continuity manager;
- workflow learner.

Its responsibility is to convert owner intent into bounded, evidence-seeking work. It should recover information from repository/project context before asking the owner to repeat it.

### 1.3 Execution agent

The coding agent:
- inspects the repository;
- implements within authority;
- runs tests;
- investigates failures;
- reports exactly what happened.

It should not silently expand product scope or take remote/destructive actions without explicit permission.

### 1.4 Independent reviewer

A reviewer is useful when separation can reveal something the implementer may miss. The reviewer should treat the implementation agent’s report as **claims to verify**, not proof.

### 1.5 Research/specialist agents

Specialist agents may be useful for separable questions such as:
- security;
- accessibility;
- vendor/runtime behavior;
- architecture alternatives;
- data/privacy implications.

Parallelism is valuable when workstreams are genuinely independent. It is harmful when agents are reasoning from unstable upstream assumptions.

### 1.6 The control-plane picture

A useful mental model is:

`Owner intent → supervising AI → governed agent run → repository change → automated/manual evidence → independent review when justified → owner acceptance`

The repository is the durable technical system of record. Chat threads are working contexts, not the canonical implementation state.

## 2. How the Supervising AI Should Talk to the User

The quality of agentic software development depends heavily on the interface between the human owner and the supervising AI.

### 2.1 Ask the user only for genuinely unavailable decisions

Before asking a question:
1. search project context;
2. inspect the repository if available;
3. inspect prior reports;
4. research mutable external behavior;
5. ask the owner only for values, preferences, approvals, or policy decisions that cannot be recovered.

Bad pattern:
> “What branch are we on? What did the last agent do? What were the approved facts?”

Better pattern:
> “The latest accepted checkpoint reports branch X and commit Y. I’ll verify that before the next run. The only decision I need from you is whether we should permit dependency Z.”

### 2.2 Distinguish owner examples from hard scope

Users often give examples rather than exhaustive specifications. The supervisor should determine whether a list is:
- binding;
- illustrative;
- incomplete by design.

If the user explicitly signals that examples are non-exhaustive (for example with “etc.” used to invite exploration), the supervisor should expand the **thinking/research space** without silently expanding implementation authority.

### 2.3 Present decisions, not noise

The owner should not be flooded with:
- routine file choices;
- recoverable repository facts;
- test command trivia;
- decisions the agent can make safely inside an approved contract.

Bring the owner:
- material product choices;
- new risk;
- architecture alternatives with trade-offs;
- security/privacy implications;
- dependency/runtime changes;
- evidence gaps that affect acceptance;
- discoveries that could change direction.

### 2.4 Never overstate status

Use explicit states such as:
- `PLANNING`
- `IMPLEMENTATION AUTHORIZED`
- `IMPLEMENTED — REVIEW PENDING`
- `CORRECTION REQUIRED`
- `TECHNICALLY ACCEPTED — MANUAL EVIDENCE PENDING`
- `CLOSED`
- `BLOCKED`

Do not say “done” when only the code is done but required review or manual evidence remains.

### 2.5 Explain why, not only what

A strong supervisor tells the user:
- what the next action is;
- why it is the right boundary;
- what is intentionally not being done;
- what evidence will determine the next decision.

### 2.6 Artifact integrity

If the user must attach a prompt, spec, closeout, or other generated artifact to an agent:
- create the actual file first;
- provide the exact filename;
- optionally provide size/hash where traceability matters;
- never tell the user to attach an artifact that does not exist.

### 2.7 Missing input should not create fake workflow history

If a run stops only because an attachment is missing and:
- authority is unchanged;
- repository state is unchanged;
- no work occurred;

resume the **same run in the same context** after supplying the missing input. Do not manufacture a new Run ID merely because delivery failed.

This pattern emerged directly in Project Atlas when a closeout synchronization run correctly stopped for a missing approved addendum; once the file was supplied, the same governed run resumed from the unchanged checkpoint.

## 3. Prompt Engineering Becomes Context and Outcome Engineering

A coding prompt should be treated as an **execution contract**, not a screenplay.

Current agent-engineering research increasingly frames the problem as context engineering or outcome engineering: provide the right context, tools, boundaries, and feedback loops; do not overload the agent with an enormous manual or prescribe every implementation detail.

### 3.1 Four-layer prompt structure

For consequential implementation work, separate:

#### A. Binding
Facts the agent may not violate:
- owner decisions;
- product invariants;
- security/privacy boundaries;
- scope;
- non-goals;
- forbidden actions;
- risk limits.

#### B. Evidence / Current Hypothesis
What current evidence suggests:
- verified repository facts;
- external research;
- likely architecture;
- likely implementation direction;
- known uncertainty.

This section is not sacred. The agent may discover a better repository-native implementation.

#### C. Acceptance Evidence
What must prove success:
- user-visible behavior;
- contract tests;
- architecture tests;
- security checks;
- recovery behavior;
- build/type/lint;
- browser/manual evidence where required.

#### D. Implementation Freedom
Explicitly authorize the agent to choose a superior implementation inside the binding constraints and require it to explain material divergence.

### 3.2 Why this matters

Over-prescriptive prompts can freeze the supervisor’s first idea into code, even when repository evidence supports something simpler or safer.

A better instruction is:
> “The current hypothesis is X. Verify it. If a smaller repository-native design satisfies the binding invariants and acceptance evidence, use it and explain why.”

### 3.3 Prompt altitude

Put stable, cross-project rules in permanent instructions.
Put repository-wide rules in repo instructions/AGENTS-style files.
Put path-specific rules near the relevant code when supported.
Put current task authority in the run prompt.

Do not paste all history into every prompt.

### 3.4 Map, not manual

Durable repository knowledge should increasingly live in:
- architecture docs;
- ADRs;
- schemas;
- tests;
- executable plans;
- closeouts;
- small AGENTS/instruction maps;
- reusable skills/scripts when repetition justifies them.

OpenAI’s agent-first engineering work reports that an oversized instruction manual crowded out useful context, while a concise map into repository-native truth worked better. GitHub similarly supports repository-wide, path-specific, agent instruction files, and task-specific skills.

## 4. Context Selection: Existing, Fresh, and Parallel

Agent context is an engineering resource.

### 4.1 Existing context

Reuse an existing agent conversation when:
- the same role continues;
- previous context remains relevant;
- local reasoning is still useful;
- the task is a direct correction of the agent’s own implementation;
- reconstruction cost would be high without adding independence.

Use **delta authority** instead of repeating history:
- previous result;
- new finding;
- new scope;
- new stop condition;
- new acceptance evidence.

### 4.2 Fresh context

Use a fresh conversation when:
- the role changes;
- independent/adversarial review matters;
- a clean architecture boundary is reached;
- prior context may bias the next decision;
- context debt has accumulated;
- cold-start recoverability is worth testing;
- alternative designs should be explored independently.

### 4.3 Context-health check

At meaningful boundaries ask:
- Is previous context still helping?
- Is it full of superseded plans and old checkpoints?
- Could the implementer’s reasoning bias the reviewer?
- Is important truth already in the repository?
- Would a fresh start test repository legibility?

### 4.4 Parallel agents

Parallelize **separable uncertainty**, not a serial critical path.

Good:
- Agent A: security analysis
- Agent B: accessibility analysis
- Agent C: architecture alternatives
- Agent D: current vendor behavior

Poor:
- Agent B implements layer 2 before Agent A stabilizes layer 1.

### 4.5 Empirical lesson from Atlas

Project Atlas initially created many fresh coding chats. Later, continuity reduced reconstruction cost. Eventually the main implementation chat accumulated enough context debt that a clean, independently accepted boundary was used to rotate into a fresh implementation chat. That fresh agent recovered the work successfully from repository truth plus a compact contract, providing evidence that repository recoverability was improving.

## 5. Run Identity: Prompt IDs, Run IDs, Chat IDs, and Checkpoints

For long-running or high-stakes AI software projects, identity discipline prevents ambiguous history.

This is optional for tiny prototypes, but highly valuable once multiple agents, reviews, or correction cycles exist.

### 5.1 Recommended identity model

**Task ID**
Defines the durable problem boundary.

Example:
`TASK-042`

**Chat / Agent Context ID**
Identifies the persistent conversation/context.

Example:
`T042-C03`

**Prompt ID**
Identifies the exact governing instruction artifact and version.

Example:
`T042-AUTH-IMPLEMENT-SESSION-BOUNDARY-v1.0`

**Run ID**
Identifies an execution/review attempt governed by a prompt.

Example:
`T042-RUN-007`

**Repository checkpoint**
Freezes the implementation state:
- repository path;
- branch;
- HEAD;
- tree when useful;
- parent;
- clean/dirty state.

### 5.2 Why Prompt ID and Run ID are different

A prompt is an instruction artifact.
A run is an execution event.

The same prompt may sometimes be resumed in the same run after a non-execution blocker such as a missing attachment.

A materially new authority or correction cycle should receive a new Prompt ID / Run ID.

### 5.3 Naming rules

Good IDs are:
- unique;
- sequential where possible;
- descriptive enough to search;
- immutable after use;
- versioned for changed prompt content.

Avoid:
- “latest prompt”;
- “review final final 2”;
- recycling an old Run ID for different authority.

### 5.4 Preflight rule

Every consequential run should verify its starting checkpoint **before editing**.

Typical preflight:
- expected repository root;
- branch;
- HEAD;
- subject;
- tree/parent if useful;
- staged/unstaged/untracked state.

If materially different:
- STOP;
- do not automatically reset, stash, clean, checkout, or repair.

This avoids an agent “fixing” the wrong repository state.

### 5.5 Prompt archival

For rigorous projects, archive consequential prompts in the repository or a durable control plane. Where exact prompt identity matters, store:
- Prompt ID;
- version;
- Run ID;
- optional byte count/hash;
- normalization rules if line endings matter.

Do not impose cryptographic prompt archival on every low-risk task. Use it when traceability and recovery justify the cost.

## 6. The Governed Agent Run

A consequential agent run should have a predictable lifecycle.

### Step 1 — Select execution configuration

Choose deliberately:
- Existing vs Fresh;
- implementation vs reviewer vs researcher;
- model;
- reasoning/effort;
- Plan/Ask vs direct execution;
- single vs parallel;
- tools;
- permissions.

Do not automatically choose the largest model, longest reasoning, or most agents.

### Step 2 — Freeze the start

Supply/verify the repository checkpoint and current authority.

### Step 3 — Reconcile reality

The agent should inspect:
- current code;
- relevant docs;
- installed versions;
- tests;
- architecture boundaries.

Plans and old reports are hypotheses until reconciled.

### Step 4 — Execute inside authority

The agent implements, investigates failures, and runs focused checks first.

### Step 5 — Classify failures before changing code

Examples:
- production defect;
- test defect;
- wrong observation boundary;
- tooling/environment;
- stale expectation;
- missing input;
- nondeterminism;
- architecture/spec conflict;
- stale external assumption.

Fix the smallest wrong layer.

### Step 6 — Run proportional evidence

Move from:
focused tests → contract/architecture → full suite → build/lint/type → integration/manual evidence as risk requires.

### Step 7 — Scope audit

Confirm what did **not** change:
- packages;
- database;
- Auth;
- remote services;
- deployment;
- unrelated product scope.

### Step 8 — Commit only if authorized

No implicit:
- push;
- PR;
- merge;
- deployment;
- destructive DB work;
- dependency addition;
- secrets changes.

### Step 9 — Return the complete report and wait

The agent stops. The supervisor reviews before issuing the next governed action.

## 7. Mandatory Report-Back: The Report Is Part of the Control System

A governed agent report is not clerical output. It is the bridge between execution and the next authority.

### 7.1 Minimum report contents

A strong run report includes:

1. setup identity;
2. Git/repository preflight;
3. work performed;
4. files changed and why;
5. architecture/data/security implications;
6. focused evidence;
7. full evidence;
8. failures and classifications;
9. scope/forbidden-change audit;
10. commit SHA/tree/parent/subject when applicable;
11. final Git/service state;
12. remaining uncertainty;
13. discoveries;
14. recommended next action;
15. exact final status/verdict.

### 7.2 Report completeness gate

The supervisor first asks:
- Is this actually the requested report?
- Are the IDs present?
- Is the checkpoint present?
- Are tests/evidence reported?
- Is final state present?
- Is there an exact verdict?

Only then should the report be judged technically.

### 7.3 No report, no chaining

If the run says “return the complete report and wait,” the next governed run must not be authorized until the report is received and reviewed.

This prevents invisible work from accumulating outside the control plane.

### 7.4 Reports are claims

Even a detailed agent report is an implementation claim. For important boundaries, reconcile it against:
- the local repository;
- tests;
- independent review;
- remote history if relevant.

### 7.5 Evidence language must be exact

A recurring failure mode is overstating evidence.

Bad:
> “maximum request size proven”

when the test measured only one large fixture.

Better:
> “largest exercised contract-valid fixture under the installed framework measured 11.9 KB; real browser-wire capture remains unproven.”

Project Atlas caught this exact issue during independent review: the implementation was safe under the configured limit, but the evidence wording was stronger than the test actually proved.

## 8. Evidence Before Acceptance: Tests Are Evidence, Not Truth

Automated tests are essential, but their value depends on whether they observe the real failure boundary.

### 8.1 Evidence stack

Possible layers:
- type system;
- unit tests;
- contract tests;
- architecture/dependency tests;
- integration tests;
- database/RLS/concurrency tests;
- production build;
- lint/format/cost guards;
- browser/network evidence;
- accessibility/device evidence;
- independent review.

Use only what the risk requires.

### 8.2 Ask of every test

- Does this test observe the real boundary?
- Could the property be false while the test passes?
- Are mocks representative?
- Did the agent change the test instead of fixing the defect?
- What remains unproven?

### 8.3 Atlas empirical evidence

**Case A — green application tests, hidden concurrency defect**
A Slice 1 implementation passed 385 automated tests. A fresh independent reviewer still found a Major defect: fixed-event wall-clock conversion depended on a time-zone fact whose concurrency baseline was not captured. The tests had not combined the cross-fact state transition that mattered.

**Case B — 461 tests, three Majors**
A production onboarding vertical passed 461 tests, architecture gates, build, lint, and typecheck. A fresh reviewer still found three Major defects:
- a recovery navigation race during pending mutation;
- no effective lossless edit path for valid sub-minute persisted timestamps;
- transitive domain coupling hidden behind a superficially “shared” UI boundary.

**Case C — architecture gate false negative**
A later correction added transitive checks, but a reviewer found the prohibited-root list incomplete. The architecture gate passed while concrete core profile policy still entered the client graph. The final solution required a stronger transitive import-graph enforcement mechanism plus negative fixtures.

The lesson is not “tests are unreliable.”
The lesson is:
> tests are only as strong as the property they actually observe.

### 8.4 Manual evidence remains separate

Source and component tests cannot prove:
- physical mobile usability;
- screen-reader behavior;
- actual browser focus sequence;
- browser-wire multipart sizes;
- real two-tab race behavior;
- deployment/runtime behavior.

Do not convert automated evidence into claims it cannot support.

## 9. Independent Review: Use It for Information Value

Independent review should be risk-triggered, not ceremonial.

### 9.1 Strong review triggers

Favor a fresh/independent reviewer for:
- authentication/authorization/RLS;
- sensitive data;
- immutable history/versioning;
- consequential concurrency;
- foundational cross-layer contracts;
- new public mutation surfaces;
- major dependencies/security changes;
- large or surprising implementations;
- behavior poorly observed by ordinary tests.

### 9.2 Reviewer prompt design

A reviewer prompt should:
- freeze the checkpoint;
- define the review scope;
- state severity taxonomy;
- treat the implementation report as claims;
- require independent diff derivation;
- require independent evidence;
- prohibit unrelated scope expansion;
- define exact verdicts.

### 9.3 Focused re-review

After a finding is corrected, do not automatically restart the entire audit.

Use:
`finding → smallest correction → affected/full evidence → focused re-review`

Broaden only if the correction creates a concrete new boundary.

### 9.4 Existing reviewer vs fresh reviewer

Reuse the same reviewer context for focused re-review when:
- the reviewer role is unchanged;
- independence from the implementer remains intact;
- the previous finding context is useful.

Use a new reviewer when:
- a full boundary has materially changed;
- a clean independent read has high value;
- the old reviewer is anchored to outdated assumptions.

### 9.5 Measure reviewer value

Track:
- Did review find a real defect?
- Did it change product/architecture?
- Was it redundant?
- Did it create scope creep?
- What was the time/compute cost?

This prevents “always review” from becoming doctrine.

## 10. Security, Permissions, and Destructive Boundaries

Coding agents should not treat all tools/actions as equally safe.

### 10.1 Explicit authority required for high-blast-radius actions

Examples:
- push;
- PR creation;
- merge;
- deployment;
- hosted service mutation;
- database reset;
- destructive migration;
- secrets rotation;
- dependency addition or mass upgrade;
- security-boundary redesign;
- use of real sensitive data.

### 10.2 Least privilege

Give the agent only the capabilities required for the task.

Prefer:
- local repository;
- local synthetic data;
- isolated worktrees;
- read-only external research;
- bounded credentials.

### 10.3 Server mutation surfaces

Treat web mutation endpoints, Server Actions, APIs, webhooks, and RPCs as directly reachable hostile-input boundaries.

Validate:
- identity;
- authorization;
- schema;
- ownership;
- concurrency baseline;
- error redaction.

Do not trust metadata merely because the UI generated it.

### 10.4 Secrets and reports

Reports should never expose:
- raw tokens;
- cookies;
- OTPs;
- database credentials;
- service-role keys;
- sensitive provider details.

### 10.5 Supply-chain changes

For new dependencies:
- verify exact package/version;
- inspect direct/transitive tree;
- inspect lock integrity;
- classify audit findings by reachability;
- do not auto-fix unrelated advisories during feature work.

A pre-existing vulnerability may still matter, but “pre-existing” and “introduced by this run” are different questions.

## 11. Failure Classification and Harness Improvement

Repeatedly telling an agent to “try again” is usually weak engineering.

### 11.1 Failure taxonomy

Before changing production code, classify:

- **Production defect** — implementation behavior is wrong.
- **Test defect** — test expectation/fixture is wrong.
- **Observation-boundary defect** — the test looks at the wrong layer.
- **Tool/environment failure** — sandbox, Docker, browser, permissions, network.
- **Nondeterminism** — flakes/races.
- **Stale expectation** — version/runtime changed.
- **Spec/architecture conflict** — requirements disagree.
- **Missing context/input** — attachment/report/decision absent.
- **Stale external assumption** — docs/package behavior changed.
- **Review-scope creep** — reviewer is inventing unrelated hardening.

### 11.2 Fix the smallest wrong layer

Do not “green the suite” by weakening the test that caught a real defect.
Do not change production to compensate for an environment failure.
Do not broaden scope because one command failed.

### 11.3 When failure should improve the harness

If the same class repeats, ask:
- Is repository guidance missing?
- Should an architecture invariant become mechanical?
- Should a script/skill replace repeated prompting?
- Is the context allocation wrong?
- Is the repository not agent-legible?

### 11.4 Project Atlas example

A transitive client architecture violation survived multiple green architecture suites because the checks observed only direct imports or incomplete prohibited roots. The eventual durable fix was not “tell the agent to remember domain neutrality harder”; it was to add a transitive import-graph boundary check and negative fixtures that fail on direct and indirect violations.

That is harness improvement: turning a repeated conceptual rule into executable evidence.

## 12. Anti-Drag: How to Avoid Building Forever

Agentic development can create endless loops of research, review, and micro-correction if no stopping discipline exists.

### 12.1 Default subphase shape

For an ordinary bounded subphase:

`reconcile/research → plan only if needed → 1–3 coherent implementation slices → verify → independent review only if justified → closeout`

This is a heuristic, not a quota.

### 12.2 Complexity alarm

If roughly 5–6 governed runs occur without completing a meaningful product/foundation boundary, ask:

- Is this real complexity?
- Did new evidence legitimately reopen assumptions?
- Are slices too small?
- Are prompts over-prescribing?
- Is review repeating itself?
- Is repository legibility causing repeated rediscovery?
- Can several serial runs be collapsed?

High-risk work can justifiably exceed this if concrete findings keep emerging.

### 12.3 Do not re-plan settled decisions

A new test failure should not automatically create a new planning phase.

Re-plan when:
- product requirement changes;
- architecture assumption is disproven;
- new external evidence materially changes the decision;
- a forbidden dependency/config/schema change becomes necessary.

### 12.4 Backlog new ideas by default

For MVPs:
- safety/correctness/pilot evidence may interrupt;
- interesting adjacent features normally go to backlog.

Do not let workflow research or infrastructure become the product.

### 12.5 “Closed” means accepted under current evidence

Later evidence may reveal a concrete defect.
Reopen the smallest affected boundary, fix it, verify it, append history, and close again.

Do not rewrite history to pretend the original closeout knew what was discovered later.

## 13. Closeout and Recovery

A long-running AI project needs a durable way to recover after context loss.

### 13.1 Closeout purpose

A closeout should allow a strong fresh agent/human to reconstruct:
- what the subphase was meant to achieve;
- what actually exists;
- repository checkpoint;
- architecture/data/security;
- verification;
- decisions;
- agent runs;
- failures and corrections;
- remaining uncertainty;
- next safe action.

### 13.2 Do not use permanent instructions as a log

Permanent instructions should contain durable principles.

Detailed history belongs in:
- repository docs;
- run reports;
- closeouts;
- ADRs;
- research notes;
- task records.

### 13.3 Recovery capsule

A compact recovery section should state:
- current milestone/subphase;
- latest accepted checkpoint;
- binding decisions;
- open risks;
- current agent contexts/roles;
- next action;
- what must be reverified.

### 13.4 Post-closeout addendum pattern

If downstream work uncovers a defect in closed work:

1. preserve original closeout unchanged;
2. narrowly reopen the affected boundary;
3. correct;
4. independently review if justified;
5. append a post-closeout addendum;
6. restore closed state.

Project Atlas used this pattern after later time-zone research exposed a historical-read compatibility defect in a closed profile-storage subphase. The original closeout remained valid evidence of what was known at the time; the addendum recorded the later discovery and correction.

## 14. Metrics and Workflow Experiments

Do not assume the current workflow is optimal merely because it works.

### 14.1 Useful metrics

Track when practical:
- first-pass correctness;
- number/severity of review findings;
- correction cycles;
- human steering time;
- agent runtime/usage;
- prompt size/style;
- Fresh vs Existing;
- model/effort;
- parallel vs serial;
- scope violations;
- report-back failures;
- missing-artifact failures;
- rework cost;
- recovery quality;
- manual evidence gaps.

### 14.2 Useful experiments

Occasionally compare:
- Existing vs Fresh implementation context;
- detailed implementation prompt vs outcome-contract prompt;
- stronger vs cheaper model;
- single agent vs Best-of-N;
- self-review vs independent review;
- one coherent larger slice vs many small slices;
- large context packet vs repository-native recovery.

Do not experiment on every task. Product delivery remains primary.

### 14.3 Model/tool assumptions expire

A harness often encodes limitations of the current model/tool. Re-evaluate when:
- models gain longer context;
- agent memory improves;
- orchestration changes;
- repository tools improve;
- previously necessary scaffolding becomes obsolete.

The method itself must remain adaptive.

## 15. Lessons Generalized from Project Atlas

Project Atlas is one project, so its evidence should not be universalized blindly. It is nevertheless a useful real-world dataset for agentic software engineering.

### Lesson 1 — Green suites do not eliminate the need for boundary-aware review

Independent reviewers repeatedly found real defects after full green suites.

General rule:
> For foundational or hard-to-observe boundaries, add independent challenge rather than assuming test volume equals coverage quality.

### Lesson 2 — Reports need exact evidence claims

Atlas reviewers repeatedly corrected claims such as “maximum” when the evidence was really “largest exercised fixture.”

General rule:
> State exactly what evidence proves, and explicitly name what remains unproven.

### Lesson 3 — Cross-fact and cross-layer dependencies are easy to miss

A wall-clock event depended on a separate time-zone fact. A stale change to that dependency could reinterpret the same user input.

General rule:
> When a field/action depends on other state, model and test the dependency baseline explicitly.

### Lesson 4 — Semantic equality matters in immutable history

Set-like values with different ordering initially created redundant revisions.

General rule:
> Define semantic equality per data type; do not let serialization accidents pollute immutable history.

### Lesson 5 — Transitive architecture matters

Moving a concrete policy import one module away can make lexical tests green while preserving the violation.

General rule:
> Foundational dependency rules should inspect the dependency graph or otherwise observe transitive behavior.

### Lesson 6 — Fail closed without trapping the user

A minute-level editor safely refused to round higher-precision stored events, but the first design gave the user no effective recovery path.

General rule:
> Safety must include a bounded usable recovery path, not only refusal.

### Lesson 7 — Fresh contexts are useful tests of repository legibility

A fresh implementation agent successfully reconstructed a large subphase using repository truth plus a compact contract.

General rule:
> Periodically test cold-start recovery. If a fresh capable agent cannot reconstruct the state, the project is relying too heavily on hidden chat context.

### Lesson 8 — Later research can legitimately reopen closed work

A downstream time-zone investigation exposed an old compatibility defect.

General rule:
> Closed work is stable by default, not immune to new evidence. Reopen only the smallest affected boundary.

### Lesson 9 — Missing transport is not a new engineering run

A missing approved artifact caused a safe STOP with zero repository effect; the same run later resumed.

General rule:
> Distinguish execution failure from input delivery failure. Do not inflate run history.

### Lesson 10 — Workflow improvements must earn permanence

Atlas changed from many Fresh chats to continuity, then later recognized context debt and reintroduced Fresh contexts at clean boundaries.

General rule:
> Treat workflow rules as hypotheses. Preserve what works, but do not turn yesterday’s workaround into permanent doctrine.

## 16. Reusable Prompt Template

Use this template for consequential implementation work.

```text
# <Project> — <Task / Outcome>

Chat/Agent Context ID:
<...>

Conversation:
Existing | Fresh

Repository:
<path>

Branch:
<branch>

Role:
<implementation / review / research>

Model / Effort:
<...>

Prompt ID:
<...>

Run ID:
<...>

Action:
<one-sentence outcome>

## 1. Binding
- owner decisions
- product invariants
- security/privacy boundaries
- scope
- non-goals
- forbidden actions
- remote/destructive permissions

## 2. Evidence / Current Hypothesis
- verified repository facts
- current research
- likely design
- known uncertainty

## 3. Acceptance Evidence
- exact user/product behavior
- focused tests
- architecture/security checks
- full gates
- manual/runtime evidence
- scope audit

## 4. Implementation Freedom
The agent may choose a superior repository-native implementation
inside the binding constraints. Explain material divergence.

## Git Preflight
- expected branch
- expected HEAD/tree/parent
- clean/dirty expectation
Mismatch → STOP; do not repair automatically.

## Report
Return the complete report and wait.
```

For small low-risk tasks, compress this aggressively.

## 17. Reusable Independent Review Template

```text
# Independent Review — <Boundary>

Role:
Independent reviewer

Conversation:
Fresh when independence matters;
Existing reviewer for focused re-review.

Frozen checkpoint:
HEAD / tree / parent / branch

Treat implementation report as claims.

## Review Scope
- exact boundaries to inspect
- explicit non-scope
- severity taxonomy

## Required Independent Evidence
- independently derive diff
- inspect implementation
- run focused tests
- run architecture/security evidence
- verify scope
- verify final Git state

## Finding Rules
A finding requires a concrete violated invariant,
reachable failure, or evidence defect.

Do not invent unrelated hardening.

## Required Verdict
PASS
PASS WITH MINOR/BACKLOG
CORRECTION REQUIRED
STOP/BLOCKER

Return complete report and wait.
```

## 18. Reusable Run Report Template

```text
# <Run ID> — <Run Title> Report

1. Setup identity
2. Git/repository preflight
3. Outcome/work performed
4. Files changed and why
5. Architecture/data/security impact
6. Focused evidence
7. Full evidence
8. Failures + classifications + corrections
9. Scope/forbidden-change audit
10. Package/DB/Auth/config effects
11. Commit SHA/tree/parent/subject
12. Final Git/service state
13. Remaining uncertainty
14. Manual evidence still required
15. Discoveries
16. Recommended next action
17. Exact final status

Return complete report and wait.
```

A reviewer should be able to tell from the report:
- what happened;
- what did not happen;
- what was proven;
- what remains unproven;
- what repository state now exists.

## 19. Project Bootstrap Checklist for AI-Native Software Development

A new project can adopt this method incrementally.

### Minimum viable harness

1. Version-controlled repository.
2. Clear product outcome and non-goals.
3. Repository instructions with build/test commands.
4. Risk/permission policy.
5. Task/run identity convention for consequential work.
6. Agent prompt template.
7. Required report-back.
8. Basic tests + type/lint/build.
9. Explicit remote/destructive action policy.
10. Closeout/recovery artifact at meaningful boundaries.

### Add when earned

- architecture tests;
- path-specific instructions;
- reusable skills;
- isolated worktrees;
- independent reviewers;
- parallel specialists;
- local observability;
- browser automation;
- test identities/fault injection;
- prompt archive hashes;
- workflow experiments.

Do not build all of this before the first product slice. Add infrastructure when risk or repeated friction justifies it.

## 20. Research Basis

This method combines empirical lessons from Project Atlas with current primary-source agent-engineering guidance.

### Primary external sources

[R1] OpenAI — *Harness engineering: leveraging Codex in an agent-first world* (2026)
https://openai.com/index/harness-engineering/

[R2] OpenAI — *How OpenAI uses Codex*
https://openai.com/business/guides-and-resources/how-openai-uses-codex/

[R3] OpenAI — *Running Codex safely at OpenAI* (2026)
https://openai.com/index/running-codex-safely/

[R4] OpenAI — *Introducing the Codex app*
https://openai.com/index/introducing-the-codex-app/

[R5] OpenAI — *How engineers at Nextdoor use Codex to build without limits*
https://openai.com/index/nextdoor/

[R6] Anthropic — *Effective context engineering for AI agents*
https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents

[R7] Anthropic — *Building Effective AI Agents*
https://www.anthropic.com/engineering/building-effective-agents

[R8] Anthropic — *Effective harnesses for long-running agents*
https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents

[R9] Anthropic — *Demystifying evals for AI agents*
https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents

[R10] GitHub Docs — repository/path/agent instruction guidance and coding-agent best practices
https://docs.github.com/en/copilot/tutorials/cloud-agent/get-the-best-results
https://docs.github.com/en/copilot/reference/custom-instructions-support

[R11] METR — *Task-Completion Time Horizons of Frontier AI Models*
https://metr.org/time-horizons/

### Project Atlas empirical evidence used

[A1] M2C-RUN-004 / M2C-RUN-005 — green Slice 1 evidence followed by a Major cross-fact concurrency finding and Minor semantic-history finding.

[A2] M2C-RUN-008 / M2C-RUN-009 — 461/461 automated tests plus architecture/build gates, followed by three Major and two Minor independent-review findings.

[A3] M2B post-closeout time-zone sequence — downstream research exposed a historical-read compatibility defect in a closed subphase; the project narrowly reopened, corrected, independently reviewed, and appended a closeout addendum.

[A4] M2C-RUN-010 / RUN-011 / RUN-012 — successive refinement of a shared UI/domain boundary showed why direct-import checks can miss transitive policy coupling and why architecture rules should become executable graph constraints.

[A5] M2B-RUN-019 missing-attachment stop/resume — a transport/input failure with zero repository effect resumed under the same governed run rather than inventing a new run.

These Atlas examples are project-specific observations. They strengthen certain hypotheses but do not by themselves establish universal software-engineering laws.
