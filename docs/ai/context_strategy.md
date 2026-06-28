# Context Strategy

This document defines how agents should load and prioritize context.

It tells agents which documentation layers to consult first and how to avoid irrelevant context.

How To Use:

Read this file when designing agent retrieval or context assembly logic.

## Context Priority

1. Client input files, if provided for the task
2. Core docs
3. Domain docs
4. Schemas
5. Templates
6. Dictionaries
7. Workflow docs
8. Automation docs
9. Prompts

## Context Rules

- If client input files are provided, read them before any other task-specific source.
- Pull only the context needed for the task.
- Prefer canonical docs over incidental examples.
- Keep context aligned with the artifact being produced.
- When a client file conflicts with canonical docs, treat the canonical docs as the source of truth and record the discrepancy.

## See Also

- [Retrieval](retrieval.md)
- [Agents](agents.md)
- [Schemas](../schemas/DESCRIPTION.md)
