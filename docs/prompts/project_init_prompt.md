# Project Init Prompt

Use this prompt to initialize a new project in the AI-First Marketing Agency.

It sets the startup context, required source docs, and the canonical artifact order for a new workspace.

How To Use:

Paste this prompt at the start of a new project task, then replace the placeholder values with the current client and project information.

```text
You are initializing a new project for the AI-First Marketing Agency.

First, read the client input files listed below, if any are provided:
- <CLIENT_INPUT_FILE_1>
- <CLIENT_INPUT_FILE_2>
- <CLIENT_INPUT_FILE_3>

If no client input files are provided, continue with the repository docs below.

Use the repository docs as the source of truth:
- docs/README.md
- docs/PROJECT.md
- docs/GLOSSARY.md
- docs/ARCHITECTURE.md
- docs/business/DESCRIPTION.md
- docs/agency/DESCRIPTION.md
- docs/marketing/DESCRIPTION.md
- docs/content/DESCRIPTION.md
- docs/design/DESCRIPTION.md
- docs/platforms/DESCRIPTION.md
- docs/prompts/DESCRIPTION.md
- docs/schemas/DESCRIPTION.md
- docs/templates/DESCRIPTION.md
- docs/workflows/DESCRIPTION.md
- docs/automation/DESCRIPTION.md
- docs/ai/DESCRIPTION.md

Create a new project workspace for:
- project name: <PROJECT_NAME>
- client/business: <CLIENT_NAME>

Seed `projects/<project_name>/project.json` from `docs/templates/project.json` and then replace placeholders with real values.

The project state must match this shape:

```json
{
  "project_name": "<PROJECT_NAME>",
  "client_name": "<CLIENT_NAME>",
  "current_stage": "client interview",
  "approved_artifacts": [],
  "next_step": "collect client interview inputs"
}
```

Use the same field names and stage wording as `docs/projects/DESCRIPTION.md`.

Then produce the initial artifacts in canonical order:
1. client_interview.json
2. marketing_brief.json
3. campaign_strategy.json
4. content_strategy.json
5. content_package.json
6. copy_package.json
7. creative_package.json
8. image_prompt_package.json
9. publishing_plan.json
10. review_report.json

Rules:
- Read any provided client input files before starting the client interview.
- Use those files to inform the interview context, missing questions, and assumptions.
- Use the canonical artifact names exactly.
- Keep one primary owner per artifact.
- Keep business, agency, marketing, content, design, platform, prompt, schema, workflow, automation, and AI concerns separate.
- If any required input is missing, stop and list the missing inputs before proceeding.
```

## See Also

- [Prompt Guidelines](prompt_guidelines.md)
- [Prompt Patterns](prompt_patterns.md)
- [AI](../ai/DESCRIPTION.md)
