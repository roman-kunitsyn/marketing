I think this is the folder that should make your project different from almost every AI marketing project.

Most AI systems know **marketing**.

Very few know **design**.

A human designer doesn't think:

> "Generate an image."

A designer thinks:

- composition
- hierarchy
- balance
- contrast
- whitespace
- typography
- color harmony
- focal point

Your AI should learn these concepts.

---

# I would actually rename it

Instead of

```text
design/
```

I'd seriously consider

```text
creative/
```

or

```text
visual_design/
```

because this folder is much broader than graphic design.

It contains visual knowledge.

---

# I would organize it like this

```text
design/

    README.md

    design_principles.md
    design_system.md

    composition.md
    hierarchy.md
    balance.md
    spacing.md
    contrast.md

    color_guidelines.md
    color_psychology.md
    color_palettes.md

    typography.md

    layouts.md
    grids.md

    branding.md

    image_sizes.md
    safe_areas.md

    image_assets.md
    iconography.md

    photography.md
    illustration.md

    prompt_translation.md

    design_checklists.md
```

Notice something.

Nothing here mentions Midjourney.

Nothing here mentions SDXL.

This is **pure design knowledge**.

---

# design_system.md

This becomes the foundation.

Defines

```text
Visual Identity

↓

Components

↓

Rules

↓

Consistency
```

It should explain

- spacing
- colors
- typography
- icons
- logo usage
- visual consistency

---

# design_principles.md

Probably the most important document.

Explain principles like

```text
Hierarchy

Contrast

Alignment

Repetition

Proximity

Balance

Emphasis

Unity

Rhythm
```

Exactly what designers learn.

---

# composition.md

One of the best AI documents.

Instead of

"beautiful image"

Teach

```text
Rule of Thirds

Leading Lines

Symmetry

Negative Space

Framing

Depth

Foreground

Background

Center Composition
```

---

# hierarchy.md

Visual hierarchy.

Explain

```text
Headline

↓

Main Object

↓

Supporting Text

↓

CTA

↓

Logo
```

---

# balance.md

Teach

```text
Symmetrical

Asymmetrical

Radial

Dynamic
```

---

# spacing.md

Explain

Whitespace

Margins

Padding

Breathing Room

---

# contrast.md

Explain

```text
Light

Dark

Color

Size

Shape

Texture
```

---

# color_guidelines.md

Not psychology.

Rules.

Example

```text
Primary

Secondary

Accent

Neutral

Background
```

---

# color_psychology.md

Different.

Explain

Blue

Trust

Green

Health

Red

Urgency

Orange

Energy

Gold

Luxury

---

# color_palettes.md

Reusable palettes.

Example

```text
Luxury

Corporate

Startup

Restaurant

Healthcare

Technology
```

---

# typography.md

Explain

Hierarchy

Headline

Subtitle

Body

Caption

Spacing

Weight

---

# layouts.md

One of the best documents.

Example

```text
Hero Layout

Grid

Split

Magazine

Minimal

Poster

Card
```

---

# grids.md

Teach

```text
2 Columns

3 Columns

12 Columns

Golden Ratio

Modular Grid
```

---

# branding.md

Explain

Logo

Identity

Voice

Recognition

Consistency

---

# image_sizes.md

Pure technical specs.

Example

Instagram

4:5

1080×1350

Facebook

1200×630

Story

1080×1920

---

# safe_areas.md

Often forgotten.

Very important.

Explain

```text
Instagram Story

Safe Area

↓

Top

↓

Bottom

↓

Center
```

Because UI overlays hide content.

---

# image_assets.md

Library.

```text
Logo

Background

Mockup

Product

Icons

Textures

Frames
```

---

# iconography.md

Explain

Flat

Outline

Filled

Minimal

3D

---

# photography.md

Amazing for AI.

Teach

```text
Lighting

Lens

Depth of Field

Perspective

Camera Angle

Framing
```

---

# illustration.md

Explain

Flat

Vector

3D

Isometric

Watercolor

Sketch

Anime

---

# prompt_translation.md

This is unique.

Teach

How design becomes prompts.

Example

Instead of

```text
Luxury
```

Translate into

```text
Elegant composition

Soft lighting

Premium materials

Minimal color palette

Gold accents

High-end editorial photography
```

This bridges design knowledge and image generation.

---

# design_checklists.md

Very practical.

Hero Image

✓ Clear hierarchy

✓ Strong focal point

✓ CTA

✓ Contrast

✓ Branding

Carousel

✓ Cover

✓ Flow

✓ Consistency

Story

✓ Safe Area

✓ Readability

✓ CTA

---

# The biggest insight

I think you're missing one abstraction.

Instead of

```text
Marketing

↓

Prompt
```

there should be

```text
Marketing

↓

Design

↓

Prompt
```

Because prompts should **never** encode business knowledge directly.

They should encode **visual decisions**.

For example:

```text
Marketing Goal

↓

Visual Style

↓

Composition

↓

Layout

↓

Color Palette

↓

Typography

↓

Image Prompt
```

This separation is incredibly powerful.

---

# My recommendation

I would organize the project around **five knowledge domains**:

```text
business/
```

Why are we doing it?

↓

```text
agency/
```

Who is responsible?

↓

```text
marketing/
```

What should we communicate?

↓

```text
content/
```

What assets should we create?

↓

```text
design/
```

**How should those assets look?**

That last question is where most AI marketing projects stop at "make it modern" or "make it premium." By explicitly documenting composition, hierarchy, color, typography, layouts, and visual language, your Creative Designer agent can make design decisions based on structured knowledge rather than relying on vague prompt wording. I think that's one of the strongest differentiators you could build into this Marketing OS.
