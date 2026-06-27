I think this folder is **the most underrated part of the entire architecture**.

Most AI projects jump directly from documentation to prompts.

I think there should be an intermediate layer:

```
Knowledge

↓

Dictionaries

↓

Schemas

↓

Artifacts

↓

AI
```

The dictionaries become your **canonical vocabulary**.

They ensure that every AI agent, every JSON artifact, every UI form, and every automation uses the same terminology.

---

# I would expand this into a complete taxonomy

```text
dictionaries/

    README.md

    marketing/

        marketing_goals.json
        campaign_types.json
        campaign_templates.json
        campaign_statuses.json

    content/

        content_types.json
        content_packages.json
        content_pillars.json
        content_statuses.json

    design/

        visual_styles.json
        color_palettes.json
        typography_styles.json
        layouts.json
        compositions.json
        lighting.json

    branding/

        brand_voices.json
        brand_personalities.json
        tone_of_voice.json

    audience/

        target_audiences.json
        industries.json
        business_types.json
        customer_personas.json

    assets/

        image_assets.json
        media_types.json
        icon_styles.json

    publishing/

        platforms.json
        publishing_statuses.json
        publishing_frequencies.json

    copywriting/

        cta_library.json
        hashtag_categories.json
        emoji_styles.json

    ai/

        image_models.json
        llm_models.json
        prompt_styles.json
```

Notice that every dictionary belongs to a business domain.

---

# README.md

This file should explain one simple rule:

> **A dictionary is the single source of truth for all enumerated values in the system.**

A dictionary should never contain business logic.

It should only contain reusable vocabulary.

---

# campaign_types.json

Not just

```json
["product_launch", "brand_awareness"]
```

Instead

```json
{
  "id": "product_launch",
  "title": "Product Launch",
  "description": "...",
  "goals": ["sales", "awareness"],
  "recommended_platforms": ["instagram", "facebook"]
}
```

Now AI understands what "Product Launch" means.

---

# content_types.json

Instead of

```json
["story", "carousel"]
```

I'd write

```json
{
  "id": "carousel",

  "purpose": "Education",

  "recommended_funnel": "consideration",

  "supports_cta": true,

  "supports_multiple_images": true
}
```

Now this becomes knowledge.

---

# content_packages.json

This is where composition happens.

Example

```json
{
  "id": "product_launch",

  "assets": ["hero_image", "carousel", "story", "offer", "faq"]
}
```

Now packages are reusable.

---

# marketing_goals.json

Instead of

```json
"lead_generation"
```

Store

```json
{
  "id": "lead_generation",

  "success_metrics": ["leads", "ctr"],

  "recommended_campaigns": ["lead_campaign"]
}
```

---

# platforms.json

One of my favorites.

Instead of

```json
"instagram"
```

Store

```json
{
  "id": "instagram",

  "supports": ["story", "carousel", "reel"],

  "preferred_ratio": "4:5",

  "supports_hashtags": true,

  "supports_links": false
}
```

Now AI knows platform capabilities.

---

# visual_styles.json

Instead of

```json
"modern"
```

Store

```json
{
  "id": "modern",

  "colors": ["neutral"],

  "composition": "minimal",

  "lighting": "soft",

  "typography": "sans-serif"
}
```

---

# brand_voices.json

Instead of

```json
"professional"
```

Store

```json
{
  "id": "professional",

  "sentence_length": "medium",

  "emoji_usage": "none",

  "tone": "expert",

  "cta_style": "formal"
}
```

---

# target_audiences.json

Instead of

```json
"restaurants"
```

Store

```json
{
  "id": "restaurant",

  "needs": ["reservations"],

  "preferred_platforms": ["instagram"],

  "typical_campaigns": ["promotion"]
}
```

---

# image_assets.json

Instead of

```json
"logo"
```

Store

```json
{
  "id": "logo",

  "category": "branding",

  "required": true
}
```

---

# color_palettes.json

Instead of

```json
"luxury"
```

Store

```json
{
  "id": "luxury",

  "colors": ["#000000", "#FFFFFF", "#D4AF37"],

  "emotion": "premium"
}
```

---

# cta_library.json

Instead of

```json
"Learn More"
```

Store

```json
{
  "id": "learn_more",

  "goal": "education",

  "funnel": "awareness",

  "tone": "neutral"
}
```

---

# The biggest architectural idea

I think your dictionaries should become **the source of every select box** in the entire system.

```
Dictionary

↓

JSON Schema

↓

Form

↓

Artifact

↓

AI
```

For example

```
marketing_goals.json

↓

client_interview.schema.json

↓

n8n Form

↓

marketing_brief.json
```

No duplicated values.

Ever.

---

# Even more interesting...

I wouldn't stop at dictionaries.

I'd introduce **three levels**.

```
Dictionary

↓

Taxonomy

↓

Ontology
```

## Dictionary

Just values.

```
Instagram

Facebook

LinkedIn
```

---

## Taxonomy

Relationships.

```
Social Media

├── Instagram
├── Facebook
├── LinkedIn
```

---

## Ontology

Meaning.

```
Instagram

supports

↓

Stories

requires

↓

Image Ratio

belongs to

↓

Social Media

recommended for

↓

Brand Awareness
```

Now your AI can **reason**, not just autocomplete.

---

# This is why I think dictionaries are one of the strongest parts of your architecture

You're not creating "lists for forms."

You're creating a **canonical business vocabulary**.

Every layer depends on it:

```
Documentation
        ↓
Dictionaries
        ↓
Schemas
        ↓
Forms
        ↓
Artifacts
        ↓
AI Agents
        ↓
Automation
```

That's exactly how large enterprise systems are built: documentation explains concepts, dictionaries standardize terminology, schemas define contracts, and runtime artifacts carry actual data. Your Marketing OS can follow the same pattern, making it consistent, extensible, and much easier to maintain over time.
