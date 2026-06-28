# LangGraph

This document defines the LangGraph execution layer for the agency.

LangGraph is used to orchestrate workflow steps and agent handoffs, but it does not redefine the workflow itself.

How To Use:

Read this file when implementing graph-based execution for the documented workflows.

## Responsibilities

- Execute workflow steps
- Route artifacts between roles or agents
- Track state transitions

## Rules

- The graph must follow the canonical workflow order.
- LangGraph should consume workflow docs, not replace them.
- Artifact contracts must remain the source of truth.

## See Also

- [Workflows](../workflows/DESCRIPTION.md)
- [Integrations](integrations.md)
- [Publishing](publishing.md)
