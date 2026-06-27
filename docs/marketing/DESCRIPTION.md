I think this folder is actually your **domain model**.

If **business/** answers:

> Why does the agency exist?

and **agency/** answers:

> Who performs the work?

then **marketing/** answers:

> What knowledge do they use to make decisions?

This folder should contain **timeless marketing knowledge**, not implementation details.

---

# I would reorganize it slightly

```text
marketing/

    README.md

    fundamentals.md
    terminology.md

    strategy.md
    marketing_goals.md

    campaign_types.md
    campaign_templates.md

    content_strategy.md
    content_pillars.md
    content_calendar.md

    target_audiences.md
    customer_personas.md

    sales_funnel.md
    customer_journey.md

    brand_voice.md
    visual_style.md

    call_to_actions.md

    metrics.md

    best_practices.md
```

Notice that none of these documents mention AI.

That's intentional.

---

# marketing_strategy.md

This is probably the most important file.

It should answer

> How do we transform business goals into marketing decisions?

For example

```text
Business Goal

↓

Marketing Goal

↓

Campaign Type

↓

Content Strategy

↓

Content Package

↓

Publishing Strategy
```

It should explain things like

- awareness campaigns
- launch campaigns
- lead generation
- engagement campaigns
- retention campaigns

---

# campaign_types.md

Defines

> What campaigns exist?

Example

```text
Product Launch

Service Launch

Brand Awareness

Lead Generation

Seasonal Campaign

Holiday Campaign

Promotion

Event Campaign

Educational Campaign

Community Campaign

Employer Branding
```

Each campaign should define

Purpose

Inputs

Outputs

Typical assets

Recommended platforms

KPIs

---

# campaign_templates.md

This is different.

Campaign Types describe ideas.

Templates describe implementation.

Example

```text
Product Launch

↓

1 Hero Image

3 Stories

1 Carousel

1 Reel

2 CTA Posts

1 FAQ
```

or

```text
Restaurant Weekly

↓

Monday Offer

Tuesday Story

Wednesday Reel

Friday Promotion

Sunday Community
```

Templates become reusable blueprints.

---

# content_pillars.md

Defines

> What topics do we repeatedly communicate?

Example

```text
Education

Products

Services

Portfolio

Testimonials

Company

Community

Lifestyle

FAQ

Industry News
```

Every campaign references multiple pillars.

---

# marketing_goals.md

Defines

Business goals.

Example

```text
Brand Awareness

Lead Generation

Sales

Engagement

Traffic

Trust

Customer Retention

Community Growth
```

Every campaign starts here.

---

# target_audiences.md

Instead of demographics...

I would classify business audiences.

Example

```text
Restaurants

Beauty

Fitness

Medical

Education

Real Estate

Software

E-commerce
```

Each audience has

Pain Points

Needs

Typical Offers

Preferred Platforms

Communication Style

---

# customer_personas.md

This goes deeper.

Example

```text
Restaurant Owner

↓

35-50

Owns one restaurant

Needs more reservations

No marketing experience

Uses Instagram
```

Personas should drive copywriting.

---

# sales_funnel.md

Defines

```text
Awareness

↓

Interest

↓

Consideration

↓

Purchase

↓

Retention

↓

Advocacy
```

Then explain

What content belongs to each stage?

Example

Awareness

Hero Images

Reels

Stories

---

Consideration

Testimonials

FAQ

Case Studies

---

Purchase

Offer

CTA

Limited Promotion

---

Retention

Customer Stories

Community

News

---

# brand_voice.md

One of the most valuable documents.

Example

```text
Professional

Friendly

Luxury

Technical

Minimal

Playful

Premium
```

Each voice defines

Vocabulary

Sentence Length

Emotion

CTA Style

Emoji Usage

Capitalization

---

# visual_style.md

The designer's bible.

Example

```text
Minimal

Corporate

Luxury

Dark

Modern

Retro

Organic

Futuristic
```

Each style defines

Color Palette

Lighting

Composition

Typography

Rendering Style

Negative Space

---

# call_to_actions.md

A surprisingly important document.

Example

```text
Learn More

Book Now

Contact Us

Schedule Demo

Start Free Trial

Order Today

Request Quote

Download Guide
```

Each CTA defines

Intent

Tone

Typical Funnel Stage

Platforms

---

# metrics.md

Marketing shouldn't end with publishing.

Document

KPIs

```text
Reach

Impressions

CTR

Engagement

Leads

Sales

ROI

CPA

ROAS
```

---

# best_practices.md

A living document.

Examples

Instagram

- 4:5 posts
- First 3 seconds matter
- CTA at the end

Facebook

- Shorter captions
- Community engagement

Image Generation

- Simple composition
- One primary message
- Strong contrast

---

# I think there is one missing concept

Something I don't see in most AI marketing projects.

```text
marketing/

↓

knowledge/

↓

strategy/

↓

execution/
```

Specifically

```text
marketing/

    knowledge/

    strategies/

    campaigns/

    templates/

    playbooks/
```

Because what you're really building is **a marketing knowledge system**, not a collection of prompts.

For example:

```text
Lead Generation Playbook

↓

Choose Audience

↓

Choose Funnel

↓

Choose Campaign

↓

Choose Content Package

↓

Choose Visual Style

↓

Generate Campaign
```

That's much more valuable than a single prompt.

---

## My recommendation

I would think of the project as **three knowledge domains**:

```text
business/
```

Business knowledge

> Why?

---

```text
agency/
```

Organizational knowledge

> Who?

---

```text
marketing/
```

Marketing knowledge

> What?

Everything else—schemas, prompts, automation, LangGraph nodes—is an implementation layer built on top of these three domains. This separation keeps the knowledge reusable regardless of whether the execution is done by Claude Code, LangGraph, n8n, or a future system.
