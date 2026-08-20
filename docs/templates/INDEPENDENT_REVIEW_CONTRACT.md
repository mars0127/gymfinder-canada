# Independent Review Contract

Use only when review has meaningful information value.

## Identity

- Issue/task:
- Reviewer:
- Conversation: Fresh / Existing reviewer for focused re-review
- Frozen branch and checkpoint:
- Implementation report location:

Treat the implementation report as claims to verify.

## Review scope

- exact boundaries;
- explicit non-scope;
- accepted invariants;
- severity taxonomy.

## Required independent evidence

- independently derive the diff;
- inspect implementation and affected contracts;
- run focused tests;
- run architecture, security, database, browser, or Figma evidence proportional to risk;
- verify scope and forbidden changes;
- verify final Git and service state.

## Finding rules

A finding requires a concrete violated invariant, reachable failure, or evidence defect. Do not invent unrelated hardening or expand product scope.

## Required verdict

Choose exactly one:

- `PASS`
- `PASS WITH MINOR/BACKLOG`
- `CORRECTION REQUIRED`
- `STOP/BLOCKER`

Return the complete review report and wait.
