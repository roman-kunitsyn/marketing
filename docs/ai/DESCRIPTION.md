I actually think this is the folder that needs the **biggest redesign**.

The more we've talked, the more I think your project is **not AI-centric**.

It's **knowledge-centric**.

AI is only one execution backend.

So I would move AI much lower in the architecture.

---

# Current architecture

```text
Knowledge

↓

AI

↓

Result
```

---

# What I would build

```text
Knowledge

↓

Artifacts

↓

Workflow

↓

Execution

↓

AI
```

AI is almost the last layer.

---

## I would even rename this folder

Instead of

```text
ai/
```

I'd call it

```text
intelligence/
```

or

```text
reasoning/
```

because it contains the reasoning layer, not just LLMs.

But `ai/` is still perfectly fine if you prefer a familiar name.

---

# I would organize it like this

```text
ai/

    README.md

    philosophy.md

    agents.md
    roles_mapping.md

    context_strategy.md
    context_loading.md

    retrieval.md

    prompt_compilation.md

    tool_usage.md

    model_selection.md

    evaluation.md

    memory.md

    reasoning.md

    planning.md

    guardrails.md
```

Notice something.

There is almost nothing here about marketing.

Everything is AI architecture.

---

# README.md

Should explain

```text
Knowledge

↓

Context

↓

Reasoning

↓

Artifact
```

The AI never invents business knowledge.

It consumes it.

---

# philosophy.md

Probably the most important document.

It should define your philosophy.

Something like

```text
Knowledge is permanent.

Artifacts are temporary.

AI is replaceable.

Execution is replaceable.

Documentation is the source of truth.
```

I think this document becomes the heart of the project.

---

# agents.md

I would not describe prompts here.

I would describe capabilities.

Example

Marketing Strategist

Reads

- Marketing Brief
- Dictionaries
- Marketing Knowledge

Produces

- Campaign Strategy

---

Creative Designer

Reads

- Campaign Strategy
- Design Knowledge

Produces

- Creative Package

---

Notice

Agents consume artifacts.

---

# roles_mapping.md

This is something you're currently missing.

Map

Business Role

↓

AI Agent

Example

```text
Marketing Strategist

↓

marketing_strategist_agent
```

---

# context_strategy.md

One of the most valuable documents.

Never dump the whole repository into context.

Instead

Marketing Strategist receives

```text
Marketing Knowledge

Campaign Types

Marketing Goals

Target Audience

Marketing Brief
```

Designer receives

```text
Creative Package

Design Knowledge

Visual Style

Brand
```

Every role gets different context.

---

# context_loading.md

Explain

How context is assembled.

Example

```text
Artifact

↓

Related Documentation

↓

Related Dictionaries

↓

Examples

↓

Prompt Compiler

↓

Model
```

---

# retrieval.md

Not "RAG."

Explain

How knowledge is selected.

For example

Marketing Goal

↓

Campaign Types

↓

Relevant Templates

↓

Examples

↓

Agent

This is retrieval based on business semantics.

---

# prompt_compilation.md

This is one of the most unique ideas.

AI should never receive

30 Markdown files.

Instead

```text
Knowledge

↓

Context Builder

↓

Compiled Prompt

↓

Model
```

The prompt is compiled.

Not handwritten.

---

# tool_usage.md

Very important.

Explain

Which tools each agent may use.

Example

Marketing Strategist

✓ Documentation

✓ Dictionaries

✓ Schemas

✗ Image Generator

---

Designer

✓ Prompt Compiler

✓ Image Generator

✓ Asset Library

---

# model_selection.md

Another missing abstraction.

Example

Reasoning

↓

Claude

Coding

↓

Codex

Image Prompting

↓

GPT-Image or Claude

Vision Review

↓

GPT-4.1 Vision

Each model has strengths.

---

# evaluation.md

Don't evaluate prompts.

Evaluate artifacts.

Example

Marketing Brief

✓ Goals

✓ Audience

✓ Platforms

---

Creative Package

✓ Composition

✓ Brand

✓ Contrast

✓ Hierarchy

---

Publishing Plan

✓ Schedule

✓ Platform

✓ Assets

---

# memory.md

I think you'll eventually need this.

Store

```text
Past Campaigns

Successful Prompts

Brand History

Client Preferences
```

Separate from the Knowledge Base.

The Knowledge Base is global.

Memory is client-specific.

---

# reasoning.md

One of my favorite documents.

Teach

How agents should think.

Example

Marketing Strategist

1. Understand business
2. Choose goals
3. Choose campaign
4. Choose content
5. Produce strategy

Designer

1. Read strategy
2. Select visual style
3. Build composition
4. Produce design specification

---

# planning.md

Different from reasoning.

Planning means

```text
Task

↓

Subtasks

↓

Dependencies

↓

Execution Order
```

Exactly what Claude Code already does well.

---

# guardrails.md

Very important.

Every agent should know

Never invent facts.

Never ignore schemas.

Never modify approved artifacts.

Always validate outputs.

Prefer dictionaries over free text.

Prefer references over assumptions.

---

# The biggest idea I would introduce

Right now

Most AI systems do

```text
System Prompt

↓

LLM

↓

Answer
```

I think your system should do

```text
Knowledge

↓

Context Builder

↓

Prompt Compiler

↓

LLM

↓

Schema Validation

↓

Artifact
```

The LLM becomes just one stage.

---

# Even more interesting...

I think there are actually **three kinds of AI** in your project.

### 1. Reasoning AI

Plans work.

Example

Claude

Codex

Gemini

---

### 2. Generative AI

Produces assets.

Example

GPT Image

Flux

SDXL

Ideogram

---

### 3. Validation AI

Reviews outputs.

Checks

- schema compliance
- brand consistency
- design quality
- copy quality

Different responsibilities.

---

# This is the architectural picture I now see

```text
Knowledge Layer
──────────────────────
business/
agency/
marketing/
content/
design/

↓

Contracts Layer
──────────────────────
dictionaries/
schemas/

↓

Process Layer
──────────────────────
workflows/

↓

Intelligence Layer
──────────────────────
Context Builder
Retrieval
Reasoning
Planning
Prompt Compiler

↓

Execution Layer
──────────────────────
Claude Code
LangGraph
Codex CLI
Gemini CLI
n8n

↓

Generation Layer
──────────────────────
GPT Image
Flux
SDXL
Midjourney
```

## One thing I would change from your original structure

I would **remove `system_prompts.md` entirely**.

After seeing the direction of your architecture, I don't think hand-written system prompts should be a core asset.

Instead, I would replace it with:

```text
prompt_compilation.md
```

because your agents shouldn't depend on static prompts. They should receive **compiled context** assembled from:

- documentation,
- dictionaries,
- schemas,
- workflows,
- examples,
- and the current artifacts.

That is much closer to how a human expert works: they don't memorize one giant instruction—they consult the relevant knowledge for the task at hand. I think this is one of the key ideas that can make your Marketing OS much more scalable than prompt-centric AI systems.
