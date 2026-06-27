I think this is the **last missing piece** of the architecture.

And I would actually change the concept slightly.

## Templates are **not examples**.

Examples show **real projects**.

Templates define **empty starting points**.

Exactly like software templates.

---

# I would expand it

```text
templates/

    README.md

    client/

        client_interview.json
        business_profile.json
        brand_profile.json

    marketing/

        marketing_brief.json
        campaign_strategy.json
        content_strategy.json

    campaign/

        campaign_package.json
        content_package.json

    content/

        copy_package.json
        creative_package.json

    generation/

        generation_specification.json
        prompt_package.json

    publishing/

        publishing_plan.json
        publishing_task.json

    reports/

        review_report.json
        analytics_report.json
        client_report.json
```

Notice something.

The structure is **identical** to `schemas/`.

That's intentional.

---

# Relationship

```
Schema

↓

Template

↓

Artifact

↓

Example
```

This is the lifecycle.

Example

```
marketing_brief.schema.json
```

↓

defines

↓

```
marketing_brief.json (template)
```

↓

used to create

↓

```
marketing_brief.json (artifact)
```

↓

stored in

↓

```
examples/software_company/
```

Beautiful symmetry.

---

# README.md

This document should explain

> Templates are starter artifacts.

They satisfy the schema.

They contain

- placeholders
- empty arrays
- default values

They never contain real client data.

---

# client/

Contains

```text
client_interview.json

business_profile.json

brand_profile.json
```

These are used by

- Web UI
- n8n
- Telegram
- CLI

---

# marketing/

Contains

Starter business artifacts.

Example

```json
{
  "marketing_goal": null,
  "campaign_type": null,
  "platforms": [],
  "target_audience": []
}
```

Not documentation.

Not schema.

Just empty.

---

# campaign/

Defines

Campaign containers.

Example

```json
{
  "campaign": {},
  "content_packages": [],
  "publishing_plan": null
}
```

---

# content/

Contains

Empty packages.

```json
{
  "hero_images": [],
  "stories": [],
  "carousels": [],
  "offers": []
}
```

---

# generation/

This is where your architecture becomes unique.

Instead of

```
prompt_package.json
```

I'd add

```
generation_specification.json
```

Example

```json
{
  "subject": null,
  "composition": null,
  "lighting": null,
  "palette": null,
  "camera": null,
  "style": null
}
```

The Prompt Compiler fills this in later.

---

# publishing/

Contains

```json
{
  "platform": null,
  "asset": null,
  "publish_at": null,
  "status": "draft"
}
```

---

# reports/

Instead of only

```
client_report.json
```

I'd add

```
review_report.json

analytics_report.json
```

Reports are outputs too.

---

# The biggest insight

Templates are **factories**.

Instead of

```
Agent

↓

JSON
```

Think

```
Template

↓

Populate

↓

Validate

↓

Artifact
```

Exactly like software objects.

---

# Even better...

I think there are actually **four levels**.

```
Documentation

↓

Schema

↓

Template

↓

Artifact
```

For example

```
marketing_brief.md
```

↓

explains

↓

```
marketing_brief.schema.json
```

↓

defines

↓

```
marketing_brief.json
```

↓

becomes

↓

```
examples/restaurant/marketing_brief.json
```

This is almost identical to

```
Interface

↓

Class

↓

Object
```

---

# One thing I would add

A **factory** layer.

```
templates/

    factories/

        marketing_brief_factory.py

        campaign_factory.py

        publishing_factory.py
```

Instead of

```python
MarketingBrief()
```

the factory creates

```
marketing_brief.json
```

pre-filled with

- default values
- dictionary references
- IDs
- timestamps
- metadata

This becomes very useful later.

---

# The final architecture

After all these discussions, I think your repository naturally forms **ten architectural layers**.

```
1. business/
```

Business knowledge

↓

```
2. agency/
```

Organization

↓

```
3. marketing/
```

Marketing knowledge

↓

```
4. content/
```

Marketing assets

↓

```
5. design/
```

Visual knowledge

↓

```
6. dictionaries/
```

Canonical vocabulary

↓

```
7. schemas/
```

Contracts

↓

```
8. templates/
```

Factories / default instances

↓

```
9. examples/
```

Reference implementations

↓

```
10. execution/
(ai/, workflows/, automation/)
```

Runtime behavior

---

## This is the strongest idea I think we've reached today

Initially, your repository looked like "documentation for an AI agent."

Now it looks much closer to **an SDK for marketing**.

A developer could:

- read the documentation,
- validate data with schemas,
- create artifacts from templates,
- inspect real examples,
- execute workflows,
- and plug in any execution engine (Claude Code, LangGraph, n8n, etc.).

In other words, you're no longer documenting prompts—you are defining an entire **Marketing Domain Model**. That makes the project much more reusable, testable, and extensible than a prompt-centric repository. I think that's a significantly stronger long-term architecture.
