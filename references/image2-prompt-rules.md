# image-2 Prompt Rules

Write the final prompt as a direct deterministic generation instruction for image-2. It should tell image-2 what to generate, in what scene, with what posture, expression, camera language, light, color, material, style, and quality.

## Required Style

- Use complete English natural language.
- Start with the main subject and scene.
- Use concrete visual relationships instead of abstract praise.
- Keep one coherent paragraph unless the user asks for another structure.
- Keep uncertainty in analysis and confidence labels, not in the final prompt.
- Choose safe definite wording when a detail is unclear.
- Avoid keyword soup such as `cinematic, beautiful, 85mm, dreamy, detailed`.
- Avoid conflicting instructions such as `soft natural documentary flash studio lighting`.
- Avoid uncertainty phrases in the final prompt: `probably`, `maybe`, `appears to`, `looks like`, `approximately`, `around`, `visually estimated`, `seems`, `might`.
- Do not include unsupported identity, brand, camera-body, lens-model, location, or original-prompt claims.

## Recommended Prompt Order

1. Subject and environment.
2. Body action and posture, including relaxed or tense body language.
3. Head angle, face direction, expression, gaze, eyes/iris detail when visible, lips, brows, skin.
4. Hair, hands, body weight, clothing, folds, and material behavior.
5. Composition: aspect ratio, framing, crop, subject scale, visual center, negative space, background relationship.
6. Camera language: angle, height, distance, finalized focal-length look, depth of field, shutter/sharpness, ISO/noise, exposure, white balance, filter/post-processing.
7. Lighting, color palette, materials, style, atmosphere, realism, and image quality.

## Phrase Patterns

Use these as patterns, not fixed templates:

- `Create a realistic editorial portrait of ...`
- `The subject stands/sits/leans ... with ...`
- `Her head is slightly turned ... while her gaze ...`
- `Frame the image in a vertical medium portrait composition ...`
- `Use an eye-level camera angle with a 50mm portrait lens look ...`
- `Use f/2.0 shallow depth of field ...`
- `Soft natural light comes from the left side of the frame ...`
- `Use a muted warm neutral palette, natural skin texture, soft fabric folds, and subtle film grain ...`

## Conservative Eye Detail

- If eye color is clear: write the visible color.
- If eye color is unclear: use `dark natural eyes`, `subtle iris detail`, or `iris color not clearly emphasized`.
- If focus is unclear: use `soft distant gaze`, `slightly unfocused expression`, or `focus level not clearly visible` in analysis.
- In the final prompt, prefer safe eye wording such as `dark natural eyes` or `soft distant gaze` instead of saying the detail is unclear.
- Do not invent pupil dilation, iris color, or gaze intensity.

## Camera Wording

Use camera details to guide generation, not to claim real metadata. Analysis may explain uncertainty. The final prompt must use determined generation wording.

Good:

- `Use a 50mm portrait lens look.`
- `Use an 85mm portrait lens look with natural background compression.`
- `Use f/2.0 shallow depth of field.`
- `Use a shutter speed fast enough to keep the subject sharp.`
- `Keep ISO low with clean shadow detail.`
- `Use subtle film-like color treatment.`

Avoid:

- `Shot on a Canon R5 with an 85mm f/1.2 lens.`
- `ISO 100, 1/250s, f/1.8` when no metadata is supplied.
- `Use a visually estimated 50mm lens.`
- `Use approximately f/2.0 depth of field.`
- `The subject probably has brown eyes.`
- `exactly the original prompt`.

## Compression Rule

Final prompts should be rich but not bloated. Prefer a single polished English paragraph that includes the decisive subject, micro-detail, composition, camera, lighting, color, material, style, and quality controls. Remove repeated adjectives and any detail not supported by the image.

## Example

Weak caption:

`A girl is standing on a street with buildings behind her.`

Strong reverse prompt:

`Create a realistic cinematic editorial portrait of a young woman standing on an urban street. Her shoulders are naturally lowered, her body weight is slightly shifted to one side, and her posture feels relaxed and effortless. Her head is slightly turned to the side, her chin is gently lowered, her lips are relaxed and slightly parted, and her eyes carry a soft distant gaze. Frame her in a vertical medium portrait composition, slightly off-center, with soft negative space above the head and a blurred urban background behind her. Use an eye-level camera angle, a 50mm portrait lens look, f/2.0 shallow depth of field, and a sharp subject with soft background bokeh. Soft natural daylight comes from the side, creating gentle facial highlights and subtle cheekbone shadows. Use muted neutral color grading, natural skin texture, soft fabric folds, subtle film grain, and a high-end fashion editorial photography atmosphere.`
