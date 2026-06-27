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
