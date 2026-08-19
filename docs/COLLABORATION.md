# Founder and AI Collaboration

## Human founders

| Role | GitHub username | Responsibilities |
|---|---|---|
| Product owner | `mars0127` | Final product direction, scope, acceptance, local context, and merge approval. |
| Second founder | `TBD` | Shared product decisions, planning, implementation ownership, and challenge of assumptions. |

Update the second founder's username after repository access is confirmed.

## Phase-specific operating model

### Planning phase — current

- The founders are the product authority.
- ChatGPT and/or Codex may act as the supervising AI, researcher, product partner, architecture partner, prompt designer, and continuity manager.
- Under the current owner decision, Claude is not part of the default planning workflow and enters when implementation is authorized.
- No production implementation is authorized yet.

### Implementation phase — later

- Codex and Claude become peer execution agents.
- Either agent may own research, planning, design, implementation, testing, debugging, documentation, or review.
- Roles are assigned per issue rather than permanently by model.
- Human founders approve material decisions and merges.

## Issue-level ownership

Every consequential issue should identify:

| Field | Meaning |
|---|---|
| Human owner | Founder accountable for the product or technical decision |
| Primary agent | Codex, Claude, ChatGPT, or none |
| Work mode | Research, planning, design, implementation, debugging, or review |
| Context | Fresh or Existing when relevant |
| Branch/worktree | Isolated work location |
| Dependencies | Upstream decisions or frozen interfaces |
| Acceptance evidence | What proves the outcome |
| Permissions | Commit, push, PR, hosted-service, dependency, or deployment authority |
| Review trigger | Whether and why independent review is required |

One primary owner prevents two agents from silently producing incompatible versions of the same feature.

## Agent-routing factors

Choose the primary agent based on the task, not a permanent hierarchy:

- current repository context;
- available tools and integrations;
- need for terminal or worktree isolation;
- need for Figma access;
- independence from prior reasoning;
- transfer cost;
- measured first-pass performance on similar GymFinder tasks;
- usage availability;
- task risk and blast radius.

Model and tool assumptions expire. Re-evaluate assignments when the tools or evidence change.

## Parallel work

Parallelize separable uncertainty or implementation, not a serial critical path.

Good examples:

- competitor pattern analysis and five-gym data calibration;
- PRD drafting and Figma information architecture after shared product assumptions are stable;
- data provenance schema and deterministic matching against a frozen contract.

Poor example:

- building result-card code while the required search-result contract is still being redesigned.

Before parallel implementation, write the shared interface or acceptance boundary first.

## Review policy

Independent review is required when it is likely to reveal information the implementer may miss. Strong triggers include:

- authentication, authorization, and RLS;
- sensitive or precise location data;
- fact history and correction integrity;
- public mutation endpoints;
- foundational schemas and cross-layer contracts;
- security or major dependency changes;
- large or difficult-to-observe implementations.

Routine documentation and low-risk isolated work may use self-verification only.

## Decision rule

- The issue owner proposes or accepts an option.
- The assigned AI or human gathers the minimum evidence needed.
- A human founder resolves material product choices.
- Important decisions are committed to `DECISIONS.md` and, when significant, an ADR.

## Disagreement rule

When founders or agents disagree:

1. State the exact decision.
2. List the viable alternatives.
3. Identify the evidence or invariant that distinguishes them.
4. Choose the smallest reversible option when evidence is weak.
5. Record the decision and review trigger.

Do not query additional AI chats until one returns the preferred answer.

## Communication hygiene

- Put accepted decisions in GitHub, not only in chat.
- Link research and Figma artifacts to the issue they inform.
- Use pull-request comments for line-specific feedback.
- Keep private participant details and credentials outside the repository.
- Close an issue only when its acceptance evidence and final state are recorded.
