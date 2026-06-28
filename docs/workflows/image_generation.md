# Image Generation Workflow

This workflow defines how generated images are handled after prompts are prepared.

It is the bridge between prompt output and visual review.

How To Use:

Read this file when implementing or validating image generation behavior.

## Inputs

- `image_prompt_package.json`
- Brand profile
- Platform context

## Steps

1. Read the prompt package.
2. Generate candidate images.
3. Compare output against the prompt intent.
4. Select or revise as needed.

## Outputs

- Generated image assets
- Revision notes, if required

## Rules

- Image generation should not invent new campaign meaning.
- Generated assets must remain compatible with the creative package.
- Quality failures should return to prompt generation or creative design.

## See Also

- [Prompt Generation](prompt_generation.md)
- [Review](review.md)
- [Design](../design/DESCRIPTION.md)
