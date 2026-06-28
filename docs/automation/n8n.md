# n8n

This document defines the n8n automation layer for the agency.

n8n can be used for forms, triggers, scheduling, and lightweight workflow orchestration.

How To Use:

Read this file when wiring forms, triggers, or scheduled jobs into the documented workflows.

## Responsibilities

- Capture client input
- Trigger workflow execution
- Schedule publishing actions
- Move artifacts between systems

## Rules

- n8n should not become the source of business logic.
- Use n8n to automate documented steps, not invent new ones.
- Keep input and output shapes aligned with schemas and templates.

## See Also

- [Workflows](../workflows/DESCRIPTION.md)
- [LangGraph](langgraph.md)
- [Integrations](integrations.md)
