# CLAUDE.md — Claude Code Project Instructions

Use `AGENTS.md` as the primary operating policy and `docs/AI_AGENT_WORKFLOW.md` as the shared agent workflow.

## Current phase

The project is in **PLANNING**. The owner has decided to conduct the current pre-implementation planning through ChatGPT and/or Codex. Claude enters the default workflow when implementation is authorized, unless that decision is formally superseded.

Do not perform planning or scaffold or implement the production application unless the repository decisions and active issue explicitly authorize that work.

## Implementation-phase role

Once implementation is authorized, Claude is a peer execution agent alongside Codex. Claude may own any suitable workstream, including:

- repository research;
- architecture;
- data modeling;
- frontend or backend implementation;
- Figma-informed design implementation;
- tests and debugging;
- security work;
- documentation;
- independent review.

Assignments are made per issue. Claude is not permanently restricted to adversarial review.

## Operating discipline

Before consequential work:

1. Inspect the active issue and relevant repository truth.
2. Verify branch and working-tree state.
3. State the outcome, scope, files, permissions, and acceptance evidence.
4. Stop rather than repairing an unexpected Git state automatically.

After work:

1. Return the complete run report required by the task.
2. State exactly what was proven and what remains unproven.
3. Identify package, database, authentication, Figma, deployment, and remote-service effects.
4. Wait for the supervising AI or human owner before chaining into a new governed task.

Use Figma tooling when configured and authorized, but do not let a visual frame override accepted product, data, privacy, or security rules.
