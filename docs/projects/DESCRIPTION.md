I actually **love this idea**. I think it's even cleaner than introducing a separate `workspace/`.

I'd make the lifecycle look like this:

```text
Knowledge Base
        │
        ▼
New Project
        │
        ▼
projects/
        │
        ▼
Review
        │
        ▼
Finished
        │
        ▼
examples/
```

This makes `examples/` a **curated library of successful projects**, not just random demos.

## I would define the repository like this

```text
marketing-agency/

    docs/
    schemas/
    dictionaries/
    templates/

    projects/
        koh-samui-charter/
        software-company/
        psychological-center/

    examples/
        restaurant/
        ecommerce/
        software-company/
```

The difference is very clear.

### `projects/`

Contains **live work**.

- incomplete
- editable
- work in progress
- reviewed by the client
- may contain drafts

---

### `examples/`

Contains **golden references**.

- completed
- approved
- cleaned
- anonymized (if needed)
- reusable for future projects
- few-shot examples for AI

---

## A project lifecycle

```text
Create Project
      │
      ▼
Client Interview
      │
      ▼
marketing_brief.json
      │
   review
      │
      ▼
campaign_strategy.json
      │
   review
      │
      ▼
creative_package.json
      │
   review
      │
      ▼
publishing_plan.json
      │
      ▼
Completed
      │
      ▼
Move to examples/
```

---

## One project

```text
projects/

    private_boat_charter/

        project.json

        client/
        strategy/
        content/
        design/
        generation/
        publishing/
        reports/
```

Everything is editable.

---

## One example

Exactly the same structure.

```text
examples/

    private_boat_charter/

        README.md

        client/
        strategy/
        content/
        design/
        generation/
        publishing/
```

But it's frozen.

No drafts.

Only approved artifacts.

---

# The thing I like most

After 30–50 completed projects, your `examples/` folder becomes an incredibly valuable dataset.

Claude Code can be instructed:

> Before creating a new campaign, search `examples/` for similar industries.

For example:

```
New client

↓

Dentist

↓

Search examples/

↓

psychological_center/
medical_clinic/
beauty_salon/

↓

Reuse patterns

↓

Generate new artifacts
```

Now the AI is learning from **your own agency's previous work**, not from generic internet examples.

---

## I would add only one thing

Inside every project:

```text
project.json
```

```json
{
  "id": "...",
  "status": "draft",

  "current_stage": "campaign_strategy",

  "approved_artifacts": ["marketing_brief"],

  "next_step": "campaign_creation"
}
```

Then Claude Code can always resume work by reading one file.

No database.

No LangGraph state.

No hidden metadata.

Everything is in Git.

---

## I think we've reached the architecture I'd actually build

```text
marketing-agency/

├── docs/             # Human & AI knowledge
├── schemas/          # Contracts
├── dictionaries/     # Canonical vocabulary
├── templates/        # Empty artifacts
├── projects/         # Active client work
├── examples/         # Completed reference projects
└── tools/            # Validation, generators, utilities (optional)
```

This is very close to how software projects are organized:

- `docs/` = documentation
- `schemas/` = interfaces/contracts
- `templates/` = scaffolding
- `projects/` = active development
- `examples/` = reference implementations

I think this architecture will scale beautifully from one client to hundreds without becoming difficult to navigate.
