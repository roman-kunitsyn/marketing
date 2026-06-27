# Frequently Asked Questions

## General

### What is the AI-First Marketing Agency?

The AI-First Marketing Agency is a knowledge-driven system that transforms structured business requirements into complete marketing campaigns.

It combines documentation, JSON schemas, AI agents, prompt engineering, and automation into a single Marketing Operating System.

---

### Is this an AI chatbot?

No.

The system is an artifact-driven workflow.

Each module produces structured business artifacts rather than engaging in free-form conversation.

---

# See Also

- [README](README.md)
- [Glossary](GLOSSARY.md)
- [Architecture](ARCHITECTURE.md)

---

# How To Use

If you start here, read [README](README.md) first for the navigation and recommended reading order.
Then use this file to resolve terminology and common questions before changing docs or implementation.

---

### What problem does the project solve?

It standardizes and automates the marketing campaign creation process.

Instead of manually creating posts, images, and publishing schedules, the system generates a complete campaign from a structured client interview.

---

## Architecture

### Why is the architecture artifact-driven?

Artifacts provide:

- deterministic outputs
- validation
- version control
- modularity
- automation
- testability

Artifacts are more reliable than passing natural language between AI agents.

---

### Why use JSON everywhere?

JSON provides:

- machine readability
- validation
- portability
- versioning
- interoperability

Every important business object can be stored, tested, and reused.

---

### Why use JSON Schema?

JSON Schema defines contracts between modules.

Benefits include:

- validation
- documentation
- code generation
- predictable interfaces
- independent module development

---

### Why maintain a Knowledge Base?

Business knowledge should not live inside prompts.

The Knowledge Base contains reusable documentation that every AI agent can reference.

This improves consistency and makes the system easier to evolve.

---

## AI Agents

### What is an agent?

An agent is a specialized worker responsible for producing one or more artifacts.

Examples:

- Marketing Strategist
- Content Strategist
- Copywriter
- Creative Designer
- Prompt Builder
- Social Media Manager
- QA Reviewer

---

### Do agents communicate directly?

No.

Agents exchange structured artifacts.

Example:

```text id="pxs67t"
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
```

---

### Can different AI providers be used?

Yes.

The architecture is AI-provider independent.

Possible providers include:

- Claude
- OpenAI
- Gemini
- Ollama

---

### Is LangGraph required?

No.

LangGraph is one possible execution engine.

The business architecture is independent from workflow orchestration.

---

### Is n8n required?

No.

n8n can be used for forms, automation, and scheduling, but it is optional.

---

## Campaigns

### What is a campaign?

A campaign is a coordinated collection of marketing assets designed to achieve specific business goals.

Examples:

- Product Launch
- Brand Awareness
- Holiday Promotion

---

### What is a Content Package?

A Content Package is a collection of related content assets.

Example:

- Hero Image
- Carousel
- Stories
- Reel
- Offer

---

### What is a Content Pillar?

A Content Pillar is a recurring category of content.

Examples:

- Education
- Portfolio
- Testimonials
- Products

---

### What is a Hero Image?

A Hero Image is the primary visual asset representing a campaign, product, or service.

It is usually the main image shown first to the audience.

---

## Prompt Engineering

### Why generate prompt packages instead of images?

Prompt packages separate creative planning from image generation.

Benefits:

- support multiple image generators
- regenerate images without redesigning campaigns
- version prompts independently
- reuse prompts across campaigns

---

### Can multiple prompt candidates be generated?

Yes.

Each image asset may contain multiple prompt variants for different visual approaches.

---

## Image Generation

### Which image generators are supported?

The architecture is model-independent.

Examples:

- Flux
- SDXL
- GPT Image
- Midjourney
- Ideogram
- Recraft

---

### Can images be regenerated later?

Yes.

Image prompts and campaign artifacts are stored separately, allowing images to be regenerated at any time.

---

## Publishing

### Which platforms are supported?

Initial support:

- Instagram
- Facebook

Future support:

- LinkedIn
- TikTok
- YouTube
- Telegram
- WhatsApp
- Pinterest

---

### How is publishing performed?

The system generates a Publishing Plan.

Publishing may occur through:

- official APIs
- browser automation
- manual export
- scheduled queues

---

### Can campaigns be prepared without publishing?

Yes.

Campaign creation and publishing are separate phases.

Publishing can be performed later or by another system.

---

## Documentation

### Why is documentation so important?

Documentation is the primary source of business knowledge.

AI agents should learn from documentation rather than relying on large, monolithic prompts.

---

### Why separate documentation into multiple files?

Benefits include:

- easier maintenance
- clearer ownership
- reusable knowledge
- faster retrieval
- modular growth

---

## Future

### Will analytics be supported?

Yes.

Future versions may include:

- engagement metrics
- conversion tracking
- campaign performance
- ROI analysis
- A/B testing

---

### Will SEO be supported?

Yes.

SEO and blog generation are planned future modules.

---

### Will video generation be supported?

Yes.

Future creative modules may generate:

- short-form videos
- reels
- promotional videos
- motion graphics

---

### Can the agency support multiple industries?

Yes.

Industry-specific templates, examples, and knowledge bases can be added without changing the core architecture.

---

## Development

### What is the first implementation milestone?

A complete documentation-first knowledge base containing:

- architecture
- glossary
- schemas
- dictionaries
- templates
- examples
- guidelines

Once the knowledge base is established, automation and AI agents can be implemented incrementally.

---

### What is the final goal?

The final objective is to build a reusable Marketing Operating System that transforms structured business requirements into complete marketing campaigns through standardized artifacts, modular AI agents, and interchangeable automation engines.

The system should remain maintainable, extensible, and independent of any single AI provider or publishing platform.
