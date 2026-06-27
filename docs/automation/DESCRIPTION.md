I think this is the folder that should contain **zero business knowledge**.

That's actually a very important architectural rule.

Everything above it:

- business
- agency
- marketing
- content
- design
- schemas
- dictionaries
- workflows

...should work even if LangGraph, n8n, and Playwright disappear tomorrow.

This folder is only about **execution**.

I would actually rename it.

Instead of

```text
automation/
```

I'd seriously consider

```text
execution/
```

because these tools execute workflows.

They don't define them.

---

# I would organize it like this

```text
execution/

    README.md

    architecture.md

    langgraph.md
    claude_code.md
    codex_cli.md
    gemini_cli.md

    n8n.md

    playwright.md
    meta_api.md

    scheduler.md

    publishing.md

    integrations.md

    deployment.md

    monitoring.md

    logging.md
```

Notice

Everything here is implementation.

Nothing here explains marketing.

---

# README.md

Should explain

```text
Knowledge

↓

Workflow

↓

Execution Engine

↓

Result
```

Execution engines are interchangeable.

---

# architecture.md

Probably the most important document.

It explains

```text
Business Layer

↓

Workflow Layer

↓

Execution Layer

↓

External Systems
```

This separation is critical.

---

# langgraph.md

Should describe

How workflows become graphs.

Example

```text
Workflow

↓

State Schema

↓

Node

↓

Edge

↓

Checkpoint

↓

Execution
```

Do **not** describe marketing.

Only orchestration.

Topics

- State
- Nodes
- Edges
- Conditional routing
- Retry
- Checkpoints
- Persistence
- Human approval

---

# claude_code.md

This is a completely different execution engine.

Explain

Claude Code executes

- documentation
- schemas
- workflows

It does not require LangGraph.

Typical usage

```text
Knowledge Base

↓

Claude Code

↓

Artifacts
```

---

# codex_cli.md

Same idea.

Explain

- project structure
- context loading
- artifact generation
- review workflow

---

# gemini_cli.md

Describe

- strengths
- limitations
- recommended workflows

---

# n8n.md

This document should explain

Where n8n fits.

Not

How n8n works.

Example

```text
Client Form

↓

Webhook

↓

Interview JSON

↓

Workflow Trigger

↓

Notification

↓

Publishing
```

Use n8n for

- forms
- scheduling
- notifications
- integrations
- approvals

Not for business logic.

---

# playwright.md

This should describe browser automation.

Example

```text
Publishing Plan

↓

Playwright

↓

Instagram

↓

Facebook
```

Topics

- login
- session handling
- uploads
- retries
- screenshots
- error recovery

---

# meta_api.md

Different.

Official publishing.

Topics

- authentication
- media upload
- scheduling
- status
- rate limits

---

# scheduler.md

This is another abstraction.

```text
Publishing Plan

↓

Queue

↓

Scheduler

↓

Publishing Backend
```

Support

- immediate
- scheduled
- recurring

---

# publishing.md

One workflow.

```text
Publishing Plan

↓

Execution

↓

Publishing Result

↓

Log
```

It shouldn't matter whether execution uses

- Meta API
- Playwright
- Manual Export

---

# integrations.md

Describe external systems.

Example

```text
CRM

Email

Cloud Storage

Google Drive

Dropbox

Slack

Telegram
```

No implementation.

Only interfaces.

---

# deployment.md

Very practical.

Possible deployments

```text
Local

Docker

Cloud

Serverless
```

Environment variables

Secrets

Storage

Volumes

---

# monitoring.md

Explain

Execution metrics.

Example

```text
Workflow Success

Execution Time

Retries

Publishing Success

Generation Cost
```

---

# logging.md

Defines logging format.

Example

```text
Workflow Started

Node Started

Node Completed

Artifact Created

Publishing Completed

Error
```

---

# The biggest architectural idea

I think this folder should never mention

```text
Marketing Goal

Campaign

Content

Design
```

Instead

Everything should talk about

```text
Workflow

State

Artifact

Execution

Retry

Queue

Checkpoint
```

This makes the execution layer reusable.

You could use the exact same execution framework for:

- Software Agency
- Marketing Agency
- Research Agency
- Design Agency

---

# Even better...

I would define an **Execution Adapter** interface.

```text
Workflow

↓

Execution Adapter

↓

LangGraph
```

or

```text
Workflow

↓

Execution Adapter

↓

Claude Code
```

or

```text
Workflow

↓

Execution Adapter

↓

n8n
```

Every engine implements the same contract.

---

# This is where I think your architecture becomes really elegant

You now have **three completely independent layers**.

```text
Knowledge Layer

Business
Agency
Marketing
Content
Design
```

↓

```text
Process Layer

Schemas

Artifacts

Workflows
```

↓

```text
Execution Layer

Claude Code

LangGraph

Codex CLI

Gemini CLI

n8n

Playwright

Meta API
```

That separation is powerful because you can replace **every tool** in the execution layer without changing your business knowledge or workflow definitions.

For example:

- Today: Claude Code + Playwright.
- Tomorrow: LangGraph + Meta Graph API.
- Next year: another orchestration framework and a different image model.

The documentation, schemas, dictionaries, and workflows remain exactly the same. That's the hallmark of a well-layered architecture: **knowledge defines what should happen, workflows define how work flows, and execution engines simply carry it out.**
