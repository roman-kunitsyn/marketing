# Context Strategy

This document defines how agents should load and prioritize context.

It tells agents which documentation layers to consult first and how to avoid irrelevant context.

How To Use:

Read this file when designing agent retrieval or context assembly logic.

## Context Priority

1. Core docs
2. Domain docs
3. Schemas
4. Templates
5. Dictionaries
6. Workflow docs
7. Automation docs
8. Prompts

## Context Rules

- Pull only the context needed for the task.
- Prefer canonical docs over incidental examples.
- Keep context aligned with the artifact being produced.

## See Also

- [Retrieval](retrieval.md)
- [Agents](agents.md)
- [Schemas](../schemas/DESCRIPTION.md)
