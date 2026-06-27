# AI-First Marketing Agency Architecture

## Overview

The AI-First Marketing Agency is an artifact-driven system.

Instead of exchanging natural language between agents, every stage produces structured artifacts that become the input for the next stage.

The architecture is designed to be:

- deterministic
- modular
- reusable
- testable
- automation-friendly
- AI-provider independent

---

# High-Level Architecture

```text
                 Client
                    │
                    ▼
           Client Interview
                    │
                    ▼
          Marketing Strategist
                    │
                    ▼
          Marketing Brief JSON
                    │
                    ▼
         Campaign Strategy JSON
                    │
                    ▼
          Content Strategist
                    │
                    ▼
         Content Strategy JSON
                    │
                    ▼
          Content Package JSON
          ┌─────────┴─────────┐
          ▼                   ▼
     Copywriter        Creative Designer
          │                   │
          ▼                   ▼
 Copy Package JSON   Creative Package JSON
                              │
                              ▼
                        Prompt Builder
                              │
                              ▼
                 Image Prompt Package JSON
                    │
                    ▼
      Social Media Manager
                    │
                    ▼
      Publishing Plan JSON
                    │
                    ▼
              QA Reviewer
                    │
                    ▼
           Review Report JSON
                    │
                    ▼
             Final Campaign
                    │
                    ▼
                 Delivery
```

---

# Architectural Principles

## Artifact Driven

Agents communicate through JSON artifacts.

Never through conversation.

Example:

```text
Marketing Brief

↓

Campaign Strategy

↓

Content Strategy

↓

Content Package

↓

Copy Package

↓

Creative Package

↓

Image Prompt Package

↓

Publishing Plan
```

---

## Knowledge Driven

Business knowledge is stored in documentation.

Examples:

- Campaign Types
- Content Types
- Platform Rules
- Prompt Guidelines
- Visual Styles
- Brand Voice
- Marketing Strategies

Agents retrieve knowledge instead of relying solely on prompts.

---

## JSON First

Every important object exists as JSON.

Examples

```text
marketing_brief.json

campaign_strategy.json

content_strategy.json

content_package.json

copy_package.json

creative_package.json

publishing_plan.json

review_report.json
```

JSON becomes the contract between modules.

---

## Platform Independent

Business logic never depends on:

- Instagram
- Facebook
- Claude
- GPT
- Gemini

Platform adapters are isolated.

---

# System Layers

```text
Presentation Layer

↓

Business Layer

↓

Knowledge Layer

↓

Generation Layer

↓

Publishing Layer

↓

Quality Layer
```

---

# Presentation Layer

Responsible for user interaction.

Possible implementations

- Web UI
- Mobile App
- Telegram Bot
- CLI
- Textual TUI
- n8n Forms

Output

Client Interview JSON

---

# Business Layer

Responsible for planning.

Contains

- Marketing Strategist
- Content Strategist

Produces

- Marketing Brief
- Campaign Strategy
- Content Strategy
- Content Package

---

# Knowledge Layer

Contains reusable business knowledge.

Includes

- Documentation
- Dictionaries
- JSON Schemas
- Examples
- Prompt Templates
- Brand Guidelines

The knowledge layer contains no executable logic.

---

# Generation Layer

Responsible for content creation.

Modules

- Copywriter
- Creative Designer
- Prompt Builder
- Image Generator

Produces

- Copy Package
- Creative Package
- Image Prompt Package

---

# Publishing Layer

Responsible for publication.

Possible backends

- Meta Graph API
- Playwright
- Manual Export
- CSV
- Queue
- Scheduler

Produces

Publishing Plan.

---

# Quality Layer

Responsible for final validation.

Contains

- QA Reviewer

Produces

- Review Report

---

# Automation Layer

Execution engines.

Examples

- Claude Code
- Codex CLI
- Gemini CLI
- LangGraph
- n8n

The business architecture must remain independent from execution engines.

---

# Core Roles

## Marketing Strategist

Creates

- marketing_brief.json
- campaign_strategy.json

---

## Content Strategist

Creates

- content_strategy.json
- content_package.json

---

## Copywriter

Creates

- copy_package.json

---

## Creative Designer

Creates

- creative_package.json

---

## Prompt Builder

Creates

- image_prompt_package.json

---

## Social Media Manager

Creates

- publishing_plan.json

---

## QA Reviewer

Creates

- review_report.json

---

# Artifact Flow

```text
client_interview.json

↓

marketing_brief.json

↓

campaign_strategy.json

↓

content_strategy.json

↓

content_package.json

├────► copy_package.json

└────► creative_package.json

                         │

                         ▼

                image_prompt_package.json

↓

publishing_plan.json

↓

review_report.json
```

Each artifact is immutable after approval.

New versions create new revisions.

---

# Knowledge Flow

```text
Knowledge Base

↓

Schemas

↓

Templates

↓

Examples

↓

Agent

↓

Artifact
```

Documentation is the primary source of truth.

---

# Image Generation Architecture

```text
Creative Package

↓

Prompt Builder

↓

Image Prompt Package

↓

Image Generator

↓

Generated Assets
```

Image generation is isolated from campaign planning.

---

# Publishing Architecture

```text
Publishing Plan

↓

Platform Adapter

↓

Instagram

Facebook

LinkedIn

TikTok
```

Every platform has its own adapter.

---

# Future Extensions

Future modules may include

- Analytics
- CRM
- Email Marketing
- Landing Page Builder
- SEO
- Blog Generator
- Video Generator
- A/B Testing
- Performance Optimization

No existing modules should require modification to support these extensions.

---

# Repository Organization

```text
docs/

roles/

guidelines/

schemas/

dictionaries/

templates/

examples/

prompts/

marketing/

platforms/

automation/
```

Documentation is organized by business domain rather than implementation.

---

# Design Philosophy

The project is not an image generator.

It is not a copywriting assistant.

It is not a social media scheduler.

It is a complete Marketing Operating System built around structured knowledge, reusable artifacts, and modular AI agents.

Every module should be independently testable, replaceable, and reusable.

The architecture favors explicit contracts (JSON Schemas) over implicit prompt behavior, making the system predictable, maintainable, and suitable for long-term evolution.
