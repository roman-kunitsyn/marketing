# Publishing

This document defines the publishing automation layer for the agency.

It covers the execution details for moving approved artifacts into platform-specific publishing systems.

How To Use:

Read this file when implementing schedule creation, post creation, or platform dispatch behavior.

## Responsibilities

- Consume approved publishing plans
- Dispatch content to platform adapters
- Record publishing status
- Report failures for review

## Rules

- Publishing automation must use approved artifacts only.
- Platform adapters must remain isolated.
- Publishing logic must not change the campaign meaning.

## See Also

- [Workflows](../workflows/DESCRIPTION.md)
- [Platforms](../platforms/DESCRIPTION.md)
- [Integrations](integrations.md)
