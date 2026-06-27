# AI-First Marketing Agency Glossary

This document defines the core terminology used throughout the project.

---

# Agency

The complete AI-powered marketing system responsible for transforming business requirements into marketing campaigns.

---

# Agent

A specialized worker responsible for producing one or more business artifacts.

Examples

- Marketing Strategist
- Copywriter
- Creative Designer

Agents never communicate directly with each other.
They communicate through structured artifacts.

---

# Artifact

A structured output produced by an agent.

Artifacts are versioned and machine-readable.

Examples

- Marketing Brief
- Campaign Strategy
- Copy Package
- Creative Package
- Publishing Plan

Artifacts are the primary communication mechanism inside the agency.

---

# Client Interview

A structured questionnaire completed by the client.

Purpose

Collect business information required to build a marketing campaign.

Output

client_interview.json

---

# Marketing Brief

The primary business document describing the client's marketing requirements.

Contains

- Business Information
- Goals
- Audience
- Platforms
- Campaign Scope
- Brand Voice

Output

marketing_brief.json

---

# Campaign

A coordinated marketing initiative designed to achieve one or more business goals.

Examples

- Product Launch
- Brand Awareness
- Holiday Promotion
- Weekly Content

A campaign consists of multiple content assets.

---

# Campaign Strategy

The implementation plan for a campaign.

Defines

- Objectives
- Content Pillars
- Publishing Frequency
- Platforms
- Success Metrics

Output

campaign_strategy.json

---

# Content Strategy

Defines how content supports marketing objectives.

Includes

- Content Pillars
- Content Mix
- Publishing Schedule
- Formats

---

# Content Package

A collection of content assets produced for a campaign.

Example

- Hero Image
- Carousel
- Story
- Reel
- CTA

---

# Content Pillar

A recurring content category used to organize marketing communication.

Examples

- Education
- Entertainment
- Portfolio
- Testimonials
- Products
- Company News

---

# Content Type

A specific type of content.

Examples

- Hero Image
- Story
- Carousel
- Reel
- Quote Card
- FAQ
- Offer

---

# Hero Image

The primary visual asset representing a campaign, product, or service.

Usually used as

- First campaign image
- Landing page banner
- Cover image
- Main promotional graphic

---

# Creative Package

A collection of visual assets produced by the Creative Designer.

Includes

- Layouts
- Visual Concepts
- Image References
- Prompt Packages

---

# Copy Package

A collection of textual assets.

Includes

- Headlines
- Captions
- CTA
- Hashtags
- Story Scripts
- Carousel Text

---

# Prompt Package

A structured collection of prompts used by image generation models.

Contains

- Positive Prompts
- Negative Prompts
- Style Instructions
- Composition
- Camera
- Lighting
- Rendering Parameters

---

# Image Prompt

A single structured instruction for generating one visual asset.

---

# Publishing Plan

Defines

- Platform
- Schedule
- Asset
- Caption
- Metadata

Output

publishing_plan.json

---

# Platform

A social media platform supported by the agency.

Examples

- Instagram
- Facebook
- LinkedIn
- TikTok

---

# Platform Adapter

A module responsible for publishing content to a specific platform.

Examples

- Meta Graph API
- Playwright
- Manual Export

Business logic never depends on adapters.

---

# Brand

The client's business identity.

Includes

- Name
- Values
- Tone
- Colors
- Typography
- Logo
- Messaging

---

# Brand Voice

The writing style used throughout marketing materials.

Examples

- Professional
- Friendly
- Luxury
- Technical
- Minimal

---

# Visual Style

The artistic direction of generated images.

Examples

- Modern
- Corporate
- Luxury
- Minimal
- Playful

---

# Target Audience

The intended audience of a marketing campaign.

May include

- Industry
- Demographics
- Interests
- Business Type
- Customer Persona

---

# Customer Persona

A fictional representation of an ideal customer.

Used during campaign planning.

---

# CTA (Call To Action)

A phrase encouraging users to perform an action.

Examples

- Contact Us
- Book Now
- Learn More
- Get Started

---

# Knowledge Base

The complete collection of documentation used by AI agents.

Includes

- Marketing knowledge
- Design guidelines
- Platform rules
- Prompt engineering
- Examples
- Schemas
- Dictionaries

The Knowledge Base is the primary source of truth.

---

# Dictionary

A reusable list of standardized values.

Examples

- Marketing Goals
- Campaign Types
- Platforms
- Visual Styles
- Brand Voices

Dictionaries improve consistency across the system.

---

# Schema

A JSON Schema defining the structure of an artifact.

Schemas serve as contracts between modules.

---

# Template

A reusable predefined document or artifact.

Templates accelerate campaign creation.

---

# Workflow

A sequence of artifact transformations.

Example

```text
Interview
    ↓
Marketing Brief
    ↓
Campaign Strategy
    ↓
Creative Package
    ↓
Publishing Plan
```

---

# Automation Engine

Software responsible for executing workflows.

Examples

- Claude Code
- Codex CLI
- LangGraph
- n8n

Automation engines orchestrate work but do not define business knowledge.

---

# Knowledge Layer

The architectural layer containing reusable documentation, schemas, dictionaries, templates, and examples.

No business execution logic belongs here.

---

# Business Layer

Responsible for marketing planning and campaign creation.

Produces structured business artifacts.

---

# Generation Layer

Responsible for generating content.

Includes

- Copywriting
- Prompt Engineering
- Image Generation

---

# Publishing Layer

Responsible for distributing completed content.

Supports multiple publishing backends.

---

# Marketing Operating System (Marketing OS)

The complete architecture combining knowledge, workflows, artifacts, AI agents, and automation into a unified system.

Marketing OS is the conceptual product implemented by this project.

---

# AI-First

A design philosophy in which AI agents are considered primary workers.

Humans supervise, review, and refine outputs rather than manually producing every artifact.

---

# Artifact-Driven Architecture

An architectural pattern where modules exchange structured artifacts instead of free-form conversations.

Artifacts are versioned, validated, reusable, and machine-readable.

This is the foundational principle of the AI-First Marketing Agency.
