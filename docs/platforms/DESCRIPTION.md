I think this folder should become **the platform knowledge layer**.

This is **not** API documentation.

This is **not** implementation.

This is:

> **How should marketing content be adapted for each platform?**

This knowledge should be usable by:

- Marketing Strategist
- Copywriter
- Designer
- Social Media Manager
- Prompt Builder

without knowing anything about Playwright or Meta API.

---

# I would actually expand it

```text
platforms/

    README.md

    instagram.md
    facebook.md
    linkedin.md
    tiktok.md
    youtube.md
    pinterest.md
    whatsapp.md
    telegram.md

    platform_comparison.md
```

---

# README.md

Explains

```text
Marketing Campaign

↓

Platform Adaptation

↓

Publishing
```

Each platform document describes

- audience
- supported content
- limitations
- best practices
- recommended campaigns

---

# instagram.md

Probably the largest document.

Sections

```text
Overview

Audience

Content Types

Image Sizes

Stories

Reels

Carousel

Feed

Captions

Hashtags

CTA

Posting Frequency

Visual Style

Brand Voice

Content Mix

Best Practices

Common Mistakes
```

---

Example

```text
Supported Content

Hero Image

Carousel

Stories

Reels

Testimonials

FAQ

Before & After

Educational Posts
```

---

Another section

```text
Recommended Image Sizes

4:5

1:1

9:16
```

---

Another

```text
Recommended Funnel

Awareness

↓

Reel

↓

Story

↓

Carousel

↓

Offer
```

---

# facebook.md

Different.

Facebook prefers

- community
- discussion
- longer captions
- links

Sections

```text
Audience

Groups

Feed

Stories

Reels

Business Pages

Content Mix

Posting Schedule

Community Building
```

---

# linkedin.md

Entirely different.

Should explain

Professional audience

Topics

Authority building

Thought leadership

Case studies

Technical posts

Hiring

Company updates

---

# tiktok.md

Should explain

Algorithm

Short videos

Hooks

Trend usage

Entertainment

Retention

Watch time

---

# youtube.md

Should explain

Long-form

Shorts

Titles

Thumbnails

Descriptions

Playlists

SEO

---

# whatsapp.md

Very different.

No feed.

Instead

```text
Broadcast

Catalog

Status

Business Profile

Automation

CRM

Customer Support
```

---

# telegram.md

Explain

Channels

Groups

Communities

Bots

Announcements

Content cadence

---

# platform_comparison.md

One of the most useful documents.

Example

| Feature      | Instagram | Facebook | LinkedIn | TikTok |
| ------------ | --------- | -------- | -------- | ------ |
| Hero Image   | ✓         | ✓        | ✓        | ✗      |
| Carousel     | ✓         | ✓        | ✓        | ✗      |
| Stories      | ✓         | ✓        | ✗        | ✗      |
| Reels        | ✓         | ✓        | ✗        | ✓      |
| Long Text    | ✗         | ✓        | ✓        | ✗      |
| Professional | ✗         | △        | ✓        | ✗      |

---

# I think every platform document should have exactly the same structure

For example

```text
1 Overview

2 Audience

3 Marketing Goals

4 Funnel Support

5 Supported Campaigns

6 Supported Content Types

7 Recommended Content Packages

8 Image Specifications

9 Copywriting Guidelines

10 Visual Guidelines

11 CTA Guidelines

12 Posting Frequency

13 Best Practices

14 Common Mistakes

15 KPIs

16 References
```

Because then AI can compare platforms automatically.

---

# Even better...

I would introduce one more abstraction.

Instead of

```text
Platform
```

Think

```text
Publishing Channel
```

Then

```text
Publishing Channel

↓

Capabilities
```

Example

```text
Instagram

Supports

Hero Image

Carousel

Story

Reel

Hashtags

CTA

Scheduling
```

Facebook

```text
Supports

Hero Image

Carousel

Community

Long Caption

External Links
```

Now imagine every platform is described by capabilities.

Then AI can do something like

```text
Campaign

↓

Required Content

↓

Find Channels
that support it

↓

Generate Assets
```

This is much more scalable.

---

# My recommendation

I would organize this folder around a **canonical platform specification**.

Every platform document should answer the same questions:

1. **Who uses this platform?**
2. **What business goals does it support?**
3. **What campaign types work well?**
4. **What content formats are available?**
5. **What technical requirements exist?**
6. **What creative best practices apply?**
7. **How should success be measured?**

If every platform follows this structure, you can later generate a `platform.schema.json` and store platform capabilities as structured data. That would let your AI automatically adapt a single campaign into platform-specific content without hardcoding rules for Instagram, Facebook, LinkedIn, or future channels.
