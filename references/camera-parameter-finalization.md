# Camera Parameter Finalization

Use this reference when converting visual uncertainty into final image-2 camera language.

## Principle

In analysis, be honest about uncertainty. In the final image-2 prompt, do not write uncertainty. Choose safe deterministic camera language that image-2 can execute.

Do not claim actual EXIF, real camera body, real lens model, true shutter, true aperture, true ISO, or true filter unless the user provides explicit evidence.

## Analysis Versus Final Prompt

Analysis can say:

- `焦距无法确认，但视觉上接近 50mm 人像视角。`
- `光圈只能根据虚化程度推断，倾向浅景深。`
- `快门不可确定，但主体清晰，没有明显运动模糊。`
- `ISO 无法确认，画面噪点较低。`

Final prompt should say:

- `Use a 50mm portrait lens look.`
- `Use f/2.0 shallow depth of field.`
- `Use a shutter fast enough to keep the subject crisp.`
- `Use low ISO with clean shadow detail.`

## Focal Length Finalization

- Wide environment with visible distortion: `Use a 24mm wide-angle lens look.`
- Natural documentary view: `Use a 35mm documentary lens look.`
- Natural portrait or uncertain portrait: `Use a 50mm portrait lens look.`
- Strong portrait compression and background separation: `Use an 85mm portrait lens look.`
- Distant compressed background: `Use a 135mm telephoto portrait look.`

When unclear, prefer `50mm portrait lens look` for people and `35mm documentary lens look` for broad environments.

## Aperture Finalization

- Deep focus scene: `Use f/8 deep focus.`
- Moderate background separation: `Use f/4 balanced depth of field.`
- Standard portrait shallow blur: `Use f/2.0 shallow depth of field.`
- Strong creamy bokeh: `Use f/1.8 shallow portrait depth of field.`

When unclear for portraits, use `f/2.0 shallow depth of field`. When unclear for architecture, product layout, or landscape, use `f/5.6 to f/8 deep focus` only if it does not contradict visible blur.

## Shutter Finalization

- Sharp still subject: `Use a shutter fast enough to keep the subject crisp.`
- Frozen action: `Use a fast shutter to freeze motion.`
- Intentional motion: `Use subtle motion blur while keeping the main subject readable.`
- Long exposure look: `Use long-exposure light trails with stable architectural detail.`

Do not write exact fractions unless supplied.

## ISO And Noise Finalization

- Clean image: `Use low ISO with clean shadow detail.`
- Night or gritty image: `Use moderate ISO with subtle digital noise.`
- Film aesthetic: `Use subtle film grain.`

Do not write exact ISO unless supplied.

## Exposure, White Balance, And Filter

- Balanced exposure: `Use balanced exposure with preserved highlights and readable shadows.`
- High-key: `Use bright high-key exposure with soft highlight rolloff.`
- Low-key: `Use low-key exposure with controlled deep shadows.`
- Warm scene: `Use warm white balance.`
- Cool scene: `Use cool white balance.`
- Mixed light: `Use mixed practical and ambient light with controlled color contrast.`
- Film look: `Use subtle film-like color treatment.`
- Clean digital look: `Use clean digital color grading.`
- Matte editorial: `Use matte editorial color grading with softened contrast.`

## Final Prompt Ban List

Do not put these uncertainty words in the final prompt:

- `probably`
- `maybe`
- `appears to`
- `looks like`
- `approximately`
- `around`
- `visually estimated`
- `seems`
- `might`
- `unclear`
- `not clearly visible`
