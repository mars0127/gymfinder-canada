# ADR-0009: Peer Implementation Agents and a Planning Control Layer

- **Status:** Accepted
- **Date:** 2026-08-19

## Context

The original repository assigned one AI agent to implementation and the other mainly to review. The founders clarified that Codex and Claude are both capable software agents and should be interchangeable across project work. The product owner also intends to conduct the current pre-implementation planning primarily through ChatGPT and/or Codex, then use both Codex and Claude during software construction.

The project needs role clarity without turning model names into permanent job titles.

## Decision

1. The human founders retain product authority and final approval.
2. During the `PLANNING` stage, ChatGPT and/or Codex act as the supervising research, planning, architecture, prompt-design, and continuity layer. Under the current owner decision, Claude enters the default workflow when implementation is authorized.
3. After implementation is authorized, Codex and Claude are peer execution agents. Either may research, design, implement, test, debug, document, or review.
4. Roles are assigned per GitHub issue according to context, tools, independence, measured performance, usage availability, and risk.
5. Each issue has one primary agent or human owner.
6. Parallel work is allowed only for separable workstreams or against a frozen shared interface.
7. Independent review is risk-triggered rather than automatic or model-specific.
8. Human founders approve material scope decisions and merges.

## Consequences

- `CLAUDE.md` no longer restricts Claude to review.
- `AGENTS.md` is the shared binding policy for all agents.
- Production implementation cannot begin merely because an agent is available; the build-ready plan must first be accepted.
- Agent performance may be observed over time, but project-specific evidence must not become a permanent universal claim about a model.
- The workflow may be revised when tools, models, or project needs change.

## Review triggers

Review this decision when:

- implementation begins;
- repeated handoff failures appear;
- one tool consistently performs better or worse on a category;
- context debt makes current conversations unreliable;
- agent capabilities or integrations materially change.
