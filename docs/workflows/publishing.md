# Publishing Workflow

This workflow defines how approved artifacts are turned into a publishing plan.

It prepares the campaign for channel-specific delivery without changing the approved content intent.

How To Use:

Read this file when implementing publishing preparation or scheduling behavior.

## Inputs

- Approved `content_package.json`
- Approved `copy_package.json`
- Approved `creative_package.json`
- Approved `image_prompt_package.json`
- Platform scope

## Steps

1. Confirm approval status.
2. Map assets to platforms.
3. Build `publishing_plan.json`.
4. Validate timing and platform fit.

## Output

- `publishing_plan.json`

## Rules

- Publishing should only use approved artifacts.
- Platform adaptation must remain consistent with the platform docs.
- Do not modify the campaign meaning during scheduling.

## See Also

- [Approval](approval.md)
- [Analytics](analytics.md)
- [Platforms](../platforms/DESCRIPTION.md)
