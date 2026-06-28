# Automation

This folder defines the execution layer.

It contains implementation details for running workflows and publishing content.
It must not introduce business knowledge or redefine the canonical artifact flow.

Use this folder for:

- workflow execution engines
- LangGraph integration
- n8n integration
- Playwright automation
- publishing adapters
- external integrations

Execution backends are interchangeable.
The business docs and artifact contracts should remain valid even if a backend changes.

How To Use:

Read [README](../README.md) first, then use this folder when implementing workflow execution or publishing automation.

Index:

- [Architecture](../ARCHITECTURE.md)
- [Workflows](../workflows/DESCRIPTION.md)
- [Projects](../projects/DESCRIPTION.md)
- [LangGraph](langgraph.md)
- [n8n](n8n.md)
- [Playwright](playwright.md)
- [Publishing](publishing.md)
- [Integrations](integrations.md)
