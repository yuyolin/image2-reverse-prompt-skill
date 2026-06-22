# image2-reverse-prompt-skill

Prompt-only Codex skill for reverse-engineering one or more reference images into deterministic English image-2 prompts.

## What It Does

This skill helps Codex analyze uploaded reference images in their original order and produce one independent image-2-ready prompt per image. It is designed for image-to-prompt workflows, not image generation.

It focuses on:

- one image, one prompt
- strict original image order
- Chinese reverse analysis
- deterministic English final image-2 prompts
- subject, pose, expression, gaze, hands, clothing, hair, composition, camera language, lighting, color, material, style, and image quality
- image-specific `Avoid / Do not include` constraints
- confidence labels and self-checks

## Boundary

This skill only generates prompts. It does not call image-2, generate images, edit images, render images, retouch images, upscale images, cut out subjects, replace backgrounds, or evaluate image-2 output.

## Installation

Copy this repository folder into your Codex skills directory, or copy the root contents into:

```text
$CODEX_HOME/skills/image2-reverse-prompt
```

If `CODEX_HOME` is not set, use your local Codex skills folder.

## Usage

Invoke the skill explicitly:

```text
$image2-reverse-prompt
```

Then upload one or more reference images and ask Codex to reverse them into image-2 prompts.

Example request:

```text
Use $image2-reverse-prompt to generate one image-2 prompt for each uploaded reference image, keeping the original order.
```

## Repository Structure

```text
.
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
|-- references/
|   |-- avoid-do-not-include-guide.md
|   |-- camera-parameter-finalization.md
|   |-- image2-prompt-rules.md
|   |-- output-template.md
|   |-- quality-and-exceptions.md
|   |-- test-checklist.md
|   `-- visual-analysis-checklists.md
`-- LICENSE
```

## License

MIT
