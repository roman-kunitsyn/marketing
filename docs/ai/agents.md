# Agents

This document defines the agent layer used by the agency.

Agents transform documentation, schemas, templates, and automation instructions into structured artifacts.

How To Use:

Read this file when designing or updating any AI role in the system.

## Agent Principles

- Each agent should own a small, clear responsibility.
- Agents should produce artifacts, not free-form operational decisions.
- Agents should rely on the documented knowledge layers.

## Canonical Agent Groups

- Planning agents
- Content production agents
- Visual direction agents
- Prompt generation agents
- QA and review agents

## Rules

- Do not make an agent the source of business truth.
- Keep agent responsibilities aligned with the canonical workflow.
- Keep artifact ownership aligned with the agency docs.

## See Also

- [Context Strategy](context_strategy.md)
- [Tool Usage](tool_usage.md)
- [Evaluation](evaluation.md)
