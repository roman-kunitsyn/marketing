# Integrations

This document defines external integration guidance for the agency.

Integrations connect the documented workflows to external services without changing the core artifact model.

How To Use:

Read this file when adding new tools, services, or platform connections.

## Integration Principles

- Keep integrations replaceable.
- Keep data contracts explicit.
- Prefer small adapter boundaries over deep coupling.

## Typical Integration Types

- Client intake forms
- Automation backends
- Publishing services
- Analytics services
- Browser automation

## Rules

- Integrations must not redefine canonical names or artifact ownership.
- Integration failures should be visible in workflow or review steps.
- The repository docs remain the source of truth for behavior.

## See Also

- [LangGraph](langgraph.md)
- [n8n](n8n.md)
- [Playwright](playwright.md)
- [Publishing](publishing.md)
