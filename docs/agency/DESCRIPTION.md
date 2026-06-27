I actually think this folder should become the **heart of the AI agency**.

Notice the difference:

- `business/` describes **how the company works**.
- `agency/` describes **how the workers work**.

This is a completely different level.

I would even expand it.

```text
agency/

    README.md

    organization.md

    roles.md
    responsibilities.md

    communication.md
    handoffs.md

    review_process.md
    approval_process.md

    quality_guidelines.md

    decision_making.md
    escalation.md

    artifact_ownership.md

    role_matrix.md
```

---

# agency/README.md

Defines the philosophy of the agency.

Example

```
Business defines WHAT.

Agency defines WHO.

Artifacts define HOW.

Automation defines WHEN.
```

---

# organization.md

Shows the organizational structure.

```
Marketing Strategist
          │
          ▼
Content Strategist
      │         │
      ▼         ▼
Copywriter   Creative Designer
      │         │
      └────┬────┘
           ▼
Social Media Manager
           │
           ▼
QA Reviewer
```

No implementation.

Only organizational relationships.

---

# roles.md

This file should be very short.

Just list every role.

```
Marketing Strategist

Content Strategist

Copywriter

Creative Designer

Social Media Manager

QA Reviewer
```

Each role links to its own documentation.

Eventually you might have

```
roles/

marketing_strategist.md

content_strategist.md

copywriter.md

designer.md
```

---

# responsibilities.md

One of the most important documents.

Instead of describing people, describe ownership.

Example

| Artifact          | Owner                |
| ----------------- | -------------------- |
| Client Interview  | Client               |
| Marketing Brief   | Marketing Strategist |
| Campaign Strategy | Content Strategist   |
| Copy Package      | Copywriter           |
| Creative Package  | Creative Designer    |
| Publishing Plan   | Social Media Manager |

Nobody edits another person's artifact without review.

---

# communication.md

Very important.

Not human chat.

Artifact communication.

Example

```
Marketing Brief

↓

Campaign Strategy

↓

Copy Package

↓

Creative Package

↓

Publishing Plan
```

Never

```
Designer asks Copywriter...

Copywriter asks Strategist...
```

Instead

```
Designer reads
Campaign Strategy
```

---

# handoffs.md

This file defines contracts.

Example

```
Marketing Brief

↓

validated?

↓

yes

↓

Content Strategist
```

Every handoff should specify

Required artifacts

Validation

Acceptance criteria

---

# review_process.md

Defines quality gates.

```
Draft

↓

Internal Review

↓

Revision

↓

Approval

↓

Client Review

↓

Final
```

Every artifact goes through exactly the same lifecycle.

---

# approval_process.md

Who approves what?

Example

```
Marketing Brief

↓

Marketing Strategist

Campaign Strategy

↓

Content Strategist

Creative Package

↓

Creative Designer

Publishing Plan

↓

Social Media Manager
```

---

# quality_guidelines.md

This becomes a checklist.

Example

Marketing Brief

✓ Goal exists

✓ Audience exists

✓ Platform selected

✓ Campaign selected

---

Creative Package

✓ Hero Image

✓ Stories

✓ Carousel

✓ Cover

---

Publishing Plan

✓ Platform

✓ Schedule

✓ Caption

✓ Assets

---

# decision_making.md

One of my favorites.

Who owns decisions?

```
Business Goal

↓

Marketing Strategist

Visual Style

↓

Creative Designer

Publishing Time

↓

Social Media Manager
```

No ambiguity.

---

# escalation.md

When something cannot be completed.

Example

```
Missing Logo

↓

Request Client

↓

Pause Workflow

↓

Resume
```

or

```
Brand Voice Missing

↓

Marketing Strategist
```

---

# artifact_ownership.md

This is almost like Git ownership.

Example

| Artifact         | Owner      | Reviewer   |
| ---------------- | ---------- | ---------- |
| Marketing Brief  | Strategist | QA         |
| Copy Package     | Copywriter | Strategist |
| Creative Package | Designer   | QA         |
| Publishing Plan  | SMM        | QA         |

---

# role_matrix.md

A compact overview.

| Role       | Creates    | Reviews    | Reads      |
| ---------- | ---------- | ---------- | ---------- |
| Strategist | Brief      | Strategy   | Interview  |
| Copywriter | Copy       | —          | Brief      |
| Designer   | Creative   | —          | Strategy   |
| SMM        | Publishing | —          | Creative   |
| QA         | Review     | Everything | Everything |

---

## My suggestion

I would actually organize the entire repository around **three layers**.

```text
business/
```

Defines

> Why does the company exist?

---

```text
agency/
```

Defines

> Who performs the work?

---

```text
marketing/
```

Defines

> What knowledge do workers use?

---

Everything else—schemas, prompts, LangGraph nodes, Claude Code tasks—is simply an implementation of those three layers.

I think this aligns very well with the way you're already designing your software agency. Instead of treating AI agents as isolated prompts, you're defining an **organization** with explicit ownership, responsibilities, and contracts. That makes the system much easier to evolve as you add new roles or automate more of the workflow.
