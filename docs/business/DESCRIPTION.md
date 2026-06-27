I actually think this is one of the most important parts of the whole project.

Almost every AI marketing project jumps directly to prompts and image generation. I would instead start from the **business process**. Everything else (roles, prompts, JSON schemas, workflows) is derived from it.

I'd organize the `business/` folder like this:

```text
business/

    README.md

    business_model.md
    service_catalog.md
    pricing.md

    client_journey.md
    workflow.md

    contracts.md
    deliverables.md
    revision_policy.md

    onboarding.md
    offboarding.md

    communication.md
```

Here's what each document should contain.

---

# business_model.md

This answers:

> **What business are we building?**

It describes the agency itself.

Example:

```text
Mission

Vision

Target Customers

Services

Value Proposition

Competitive Advantages

Business Model

Revenue Streams

Customer Lifecycle

Success Metrics
```

Example:

```text
Client

↓

Marketing Campaign

↓

Content Production

↓

Publishing

↓

Analytics

↓

Long-term Partnership
```

---

# pricing.md

This is **not just prices**.

It describes how the agency sells work.

Example

```text
One-time Campaign

Monthly Subscription

Campaign Audit

Content Production

Prompt Engineering

Publishing

Automation Setup
```

Example packages

```text
Starter

Professional

Business

Enterprise
```

---

# service_catalog.md

One of my favorites.

This becomes a dictionary of services.

Example

```text
Marketing Strategy

Brand Audit

Campaign Design

Copywriting

Image Generation

Publishing

Automation

Analytics

SEO

Landing Pages
```

Every service should define

- description
- inputs
- outputs
- deliverables
- required artifacts

---

# workflow.md

Probably the most important document.

This describes the business process.

Example

```text
Lead

↓

Discovery Call

↓

Client Interview

↓

Marketing Brief

↓

Proposal

↓

Approval

↓

Campaign Production

↓

Review

↓

Publishing

↓

Analytics
```

Every step should define

- responsible role
- input
- output
- exit criteria

---

# client_journey.md

This is **the customer's experience**.

Example

```text
Visitor

↓

Lead

↓

Client

↓

Active Campaign

↓

Monthly Customer

↓

Long-term Partner
```

Every stage answers

- what does the client expect?
- what information do we collect?
- what artifacts are produced?
- what communication happens?

---

# contracts.md

This is surprisingly useful for AI.

Instead of legal language, describe business contracts.

Example

```text
Project Scope

Deliverables

Timeline

Approval Process

Revision Policy

Ownership

Payment Terms

Communication Rules
```

Because later your AI can automatically generate proposals.

---

# deliverables.md

Defines exactly what the client receives.

Example

```text
Marketing Brief

Campaign Strategy

Instagram Package

Facebook Package

Image Assets

Prompt Package

Publishing Calendar

Documentation
```

Each deliverable should define

- format
- owner
- schema
- acceptance criteria

---

# revision_policy.md

This is very useful for automation.

Example

```text
Client Review

↓

Revision Request

↓

Artifact Update

↓

Approval
```

Defines

- how revisions work
- versioning
- approval states

---

# onboarding.md

Everything before work starts.

```text
Questionnaire

Brand Assets

Logos

Fonts

Access

Social Accounts

Business Information
```

---

# communication.md

Defines communication rules.

Example

```text
Discovery Meeting

Weekly Update

Review Meeting

Campaign Approval

Delivery
```

---

# Why I think this folder is so important

I would actually consider **business/** to be the highest layer of the architecture.

```text
Business
    │
    ▼
Workflow
    │
    ▼
Roles
    │
    ▼
Artifacts
    │
    ▼
Schemas
    │
    ▼
AI Agents
    │
    ▼
Automation
```

Notice the direction.

Most AI projects start with:

```
LLM
↓

Prompt
↓

Hope
```

I would build it in the opposite direction:

```
Business Model

↓

Business Workflow

↓

Roles

↓

Artifacts

↓

JSON Schemas

↓

Knowledge Base

↓

AI Agents

↓

LangGraph / Claude Code / n8n
```

I think this fits your philosophy much better. You've consistently designed your software agency around explicit artifacts and responsibilities rather than around prompts. Applying the same principle here means the marketing agency's **business model becomes the source of truth**, and the AI implementation simply executes that well-defined business process.
