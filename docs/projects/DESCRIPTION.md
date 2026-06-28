# Projects

This folder contains live, editable workspaces.

Projects are in-progress campaigns that move through the canonical flow from client interview to delivery.
Approved work can later be curated into `examples/`.

Use this folder for:

- active client work
- drafts and revisions
- project state files
- approved artifact tracking

Recommended project metadata:

- `project.json`
- current stage
- approved artifacts
- next step

Projects are mutable.
Examples are curated and frozen.

How To Use:

Read [README](../README.md) first, then use this folder for active work in progress.

## Recommended Workspace Structure

Each live project should keep its own working files together in a single folder:

```text
projects/<project_name>/
├── project.json
├── client_inputs/
├── artefacts/
└── prompts/
```

### client_inputs/

- Landing page exports
- Client notes
- Brand assets
- Reference files
- Interview source material

### artefacts/

- client_interview.json
- marketing_brief.json
- campaign_strategy.json
- content_strategy.json
- content_package.json
- copy_package.json
- creative_package.json
- image_prompt_package.json
- publishing_plan.json
- review_report.json

### prompts/

- Generated prompts
- Prompt order
- Prompt revisions
- Prompt version history

### project.json

- current stage
- approved artifacts
- next step
- project metadata

Example shape:

```json
{
  "project_name": "<PROJECT_NAME>",
  "client_name": "<CLIENT_NAME>",
  "current_stage": "client interview",
  "approved_artifacts": [],
  "next_step": "collect client interview inputs"
}
```

Use this structure to keep inputs, generated outputs, and prompt history separated but easy to navigate.

Index:

- [Templates](../templates/DESCRIPTION.md)
- [Examples](../examples/DESCRIPTION.md)
- [Schemas](../schemas/DESCRIPTION.md)
- [Psychological Center](psychological_center/project.json)
- [Private Boat Charter](private_boat_charter/project.json)
- [Ecommerce](ecommerce/project.json)
