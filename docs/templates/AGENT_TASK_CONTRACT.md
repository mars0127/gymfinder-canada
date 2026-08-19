# Agent Task Contract

Use this template for consequential planning, design, implementation, or correction work. Compress it for low-risk tasks.

## Identity

- Task / issue ID:
- Context ID, when useful:
- Prompt/contract version, when useful:
- Run ID, when useful:
- Human owner:
- Primary agent:
- Work mode:
- Conversation: Fresh / Existing
- Repository:
- Branch/worktree:
- Expected starting checkpoint:

## Outcome

What must become true after this task?

## 1. Binding

- accepted owner decisions;
- product and data invariants;
- security/privacy boundaries;
- scope;
- non-goals;
- forbidden actions;
- remote/destructive permissions.

## 2. Evidence / current hypothesis

- verified repository facts;
- current research;
- likely design or architecture;
- known uncertainty;
- upstream interfaces or Figma frames.

This section is a hypothesis unless explicitly marked binding.

## 3. Acceptance evidence

- exact behavior or artifact;
- focused tests or checks;
- architecture/security evidence;
- build, type, lint, or schema evidence;
- Figma or browser evidence when required;
- scope audit;
- required report and final status.

## 4. Implementation freedom

The agent may choose a superior repository-native solution inside the binding constraints. Explain material divergence.

## Git preflight

Verify branch, HEAD, and working state before editing. A material mismatch means stop; do not reset, stash, clean, checkout, or repair automatically.

## Report

Return the complete run report and wait.
