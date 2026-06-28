# Approval Workflow

This workflow defines how artifacts are approved after review.

It is the decision gate between QA and delivery.

How To Use:

Read this file when implementing acceptance logic or client approval steps.

## Inputs

- `review_report.json`
- Client feedback, if applicable
- Revision notes

## Steps

1. Evaluate review outcomes.
2. Apply requested revisions if needed.
3. Confirm final acceptance.
4. Mark the package ready for publishing or delivery.

## Output

- Approved campaign package

## Rules

- Do not approve unresolved review issues.
- Approval should be explicit and traceable.
- Approval must follow review, not replace it.

## See Also

- [Review](review.md)
- [Publishing](publishing.md)
- [Business](../business/DESCRIPTION.md)
