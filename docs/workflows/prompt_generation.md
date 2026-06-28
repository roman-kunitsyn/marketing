# Prompt Generation Workflow

This workflow defines how image prompts are produced from creative direction.

It converts the creative package into structured image prompt instructions.

How To Use:

Read this file when preparing prompt packages for image generation.

## Inputs

- `creative_package.json`
- Design system
- Visual style
- Brand profile

## Steps

1. Review the creative package.
2. Draft positive and negative prompts for each asset.
3. Add style notes where useful.
4. Produce `image_prompt_package.json`.
5. Validate the prompts against the creative intent.

## Output

- `image_prompt_package.json`

## Rules

- Prompts must be traceable to the creative package.
- Do not change the campaign meaning while generating prompts.
- Keep prompt instructions concise and model-friendly.

## See Also

- [Creative Design](creative_design.md)
- [Image Generation](image_generation.md)
- [Prompts](../prompts/DESCRIPTION.md)
