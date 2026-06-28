# AI-First Marketing Agency

## Mission

Build an AI-first content marketing agency that transforms a client interview into a complete marketing campaign, including strategy, copywriting, image prompts, creative assets, publishing plans, and automation.

The agency is knowledge-driven. Every decision is based on structured documentation, reusable schemas, and JSON artifacts instead of ad-hoc prompts.

---

# See Also

- [README](README.md)
- [Architecture](ARCHITECTURE.md)
- [Glossary](GLOSSARY.md)
- [Roadmap](ROADMAP.md)

---

# How To Use

If you start here, read [README](README.md) first for the navigation and recommended reading order.
Then use this file to understand the canonical artifact flow, roles, and implementation state.

---

# Project Kickoff

When starting a new project:

1. Read any client input files first, if they are available.
2. Confirm the project name and client name.
3. Start from `client_interview.json`.
4. Move through the canonical artifact flow in order.
5. Save project state in `projects/<project_name>/project.json`.

---

# Core Principles

- AI First
- Knowledge Driven
- JSON First
- Artifact Driven
- Modular
- Platform Independent
- Human Review Optional
- Deterministic Workflows

---

# Workflow

```
Client

↓

Interview

↓

Marketing Brief

↓

Campaign Strategy

↓

Content Strategy

↓

Content Package

        ├────► Copy Package
        └────► Creative Package
                         │
                         ▼
                Image Prompt Package

↓

Publishing Plan

↓

Review

↓

Delivery
```

---

# Agency Roles

## Marketing Strategist

Purpose

Convert business requirements into a marketing strategy.

Input

- Client Interview
- Brand Information

Output

- marketing_brief.json
- campaign_strategy.json

---

## Content Strategist

Purpose

Design the content plan.

Responsibilities

- Content Pillars
- Campaign Types
- Content Packages
- Publishing Frequency

Output

- content_strategy.json
- content_package.json

---

## Copywriter

Purpose

Generate all written content.

Produces

- Headlines
- Captions
- CTA
- Stories
- Carousel Text
- Hashtags

Output

- copy_package.json

---

## Creative Designer

Purpose

Create the visual concept.

Produces

- Hero Images
- Carousel Concepts
- Story Concepts
- Reel Covers

Output

- creative_package.json

---

## Prompt Builder

Purpose

Generate image prompt packages.

Output

- image_prompt_package.json

---

## Social Media Manager

Purpose

Prepare platform-specific publishing.

Produces

- Publishing Schedule
- Platform Adaptation
- Metadata
- Publishing Queue

Output

- publishing_plan.json

---

## QA Reviewer

Purpose

Validate the final campaign artifacts.

Output

- review_report.json

---

# Main Artifacts

```
client_interview.json

↓

marketing_brief.json

↓

campaign_strategy.json

↓

content_strategy.json

↓

content_package.json

↓

copy_package.json

↓

creative_package.json

↓

image_prompt_package.json

↓

publishing_plan.json

↓

review_report.json
```

---

# Marketing Concepts

## Campaign Types

- Product Launch
- Service Launch
- Brand Awareness
- Weekly Content
- Monthly Content
- Holiday Campaign
- Sales Campaign
- Event Promotion
- Customer Story
- Portfolio Showcase

---

## Content Types

- Hero Image
- Single Image
- Carousel
- Story
- Reel
- Educational Post
- Testimonial
- FAQ
- Quote
- Case Study
- Product Showcase
- Before & After
- Behind the Scenes
- Announcement
- Offer

---

## Content Pillars

- Education
- Entertainment
- Products
- Services
- Portfolio
- Testimonials
- Company
- Community
- Lifestyle
- FAQ
- Industry News

---

## Marketing Goals

- Brand Awareness
- Lead Generation
- Sales
- Community Growth
- Customer Retention
- Website Traffic
- Product Launch
- Trust Building

---

# Platforms

Initially supported

- Instagram
- Facebook

Future

- LinkedIn
- TikTok
- YouTube
- WhatsApp
- Telegram
- Pinterest

---

# Knowledge Base

The agency relies on structured documentation.

Knowledge categories include:

- Marketing
- Branding
- Design
- Copywriting
- Prompt Engineering
- Social Media
- Platform Guidelines
- Image Generation
- Publishing
- Analytics

---

# Dictionaries

The system uses reusable dictionaries.

Examples

- campaign_types.json
- content_types.json
- marketing_goals.json
- visual_styles.json
- target_audiences.json
- brand_voices.json
- image_assets.json

---

# Schemas

All artifacts are defined by JSON Schema.

Examples

- marketing_brief.schema.json
- campaign_strategy.schema.json
- content_strategy.schema.json
- content_package.schema.json
- copy_package.schema.json
- creative_package.schema.json
- image_prompt_package.schema.json
- publishing_plan.schema.json
- review_report.schema.json

---

# Automation

The workflow should not depend on a specific implementation.

Possible execution engines

- Claude Code
- Codex CLI
- Gemini CLI
- LangGraph
- n8n

---

# Publishing

Publishing is separated from campaign creation.

Possible publishing backends

- Meta API
- Playwright
- Manual Export
- CSV
- Scheduled Queue

---

# Project Structure

```
Knowledge Base
        │
        ▼
Client Interview
        │
        ▼
Marketing Brief
        │
        ▼
Campaign Strategy
        │
        ▼
Content Strategy
        │
        ▼
Content Package
        ├────► Copy Package
        └────► Creative Package
                         │
                         ▼
                Image Prompt Package
        │
        ▼
Publishing
        │
        ▼
Review
        │
        ▼
Delivery
```

---

# Future Extensions

- Analytics
- A/B Testing
- CRM Integration
- Email Campaigns
- SEO
- Blog Generation
- Landing Pages
- Video Generation
- Marketing Automation
- Performance Reporting
- Multi-language Campaigns

---

# Design Philosophy

The agency does not generate isolated images or posts.

It generates complete marketing campaigns composed of structured artifacts.

Every artifact is machine-readable, reusable, version-controlled, and can be consumed by AI agents, automation systems, or human specialists.
