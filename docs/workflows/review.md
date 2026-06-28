# Review Workflow

This workflow defines how produced artifacts are reviewed.

It ensures the full package is internally consistent before approval or delivery.

How To Use:

Read this file when implementing QA checks or revision loops.

## Inputs

- `content_package.json`
- `copy_package.json`
- `creative_package.json`
- `image_prompt_package.json`
- `publishing_plan.json`

## Steps

1. Check completeness.
2. Check naming and schema alignment.
3. Check cross-artifact consistency.
4. Record issues in `review_report.json`.

## Output

- `review_report.json`

## Rules

- Review should catch inconsistencies before delivery.
- A failed review returns the artifact to its owner.
- Review notes should be specific and actionable.

## See Also

- [Approval](approval.md)
- [Publishing](publishing.md)
- [Agency](../agency/DESCRIPTION.md)
