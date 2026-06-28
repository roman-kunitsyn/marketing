# Client Interview Workflow

This workflow defines how the client interview stage is completed.

It turns discovery inputs into a structured artifact that starts the rest of the pipeline.

How To Use:

Read this file when collecting client requirements or implementing interview intake.

## Inputs

- Client input files, if provided
- Lead or client request
- Discovery notes
- Business goals
- Platform scope
- Brand context

## Steps

1. Collect client information.
2. Read any provided client input files first.
3. Clarify goals, scope, and platforms.
4. Normalize notes into `client_interview.json`.
5. Validate completeness before handoff.

## Output

- `client_interview.json`

## Rules

- If client input files are provided, read them before starting the interview.
- Do not start strategy before the interview is complete.
- Keep the interview structured and repeatable.
- Capture only information that is useful downstream.

## See Also

- [Campaign Creation](campaign_creation.md)
- [Agency](../agency/DESCRIPTION.md)
- [Business](../business/DESCRIPTION.md)
