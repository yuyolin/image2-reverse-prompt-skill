---
name: image2-reverse-prompt
description: Reverse-engineer one or more uploaded reference images into separate, copy-ready English image-2 generation prompts. Use when the user uploads or references images and asks for prompts, reverse prompts, image-to-prompt conversion, prompt extraction, composition analysis, camera/lens finalization, or image-2-specific AI image prompts. Preserve original image order, produce exactly one prompt per image, only generate prompts, never generate/edit/render images, and include Chinese reverse analysis, a deterministic English final image-2 prompt, Avoid / Do not include, confidence labels, and a self-check unless the user requests another format.
---

# Image2 Reverse Prompt

## Core Contract

Treat the task as image-to-image-2 prompt reverse engineering, not ordinary captioning. Convert each visible image into deterministic English instructions that would help image-2 recreate a similar visual result.

This skill only generates image-2-ready reverse prompts. It does not generate, edit, render, upscale, cut out, retouch, modify, or evaluate images.

Always:

- Preserve the user's original image order.
- Produce exactly one independent result for each image.
- Only output prompt work: analysis, final prompt, Avoid / Do not include, confidence labels, and self-check.
- Keep analysis and final prompts separate so the user can copy the prompt directly.
- Base all claims on visible evidence, user-provided context, or EXIF/metadata explicitly available in the conversation.
- Mark uncertain details with confidence labels and conservative wording.
- Write the final image-2 prompt in clear, complete, deterministic English natural language, not scattered keywords.
- Keep uncertainty in the analysis and confidence labels; do not put uncertainty words in the final prompt.
- Default to Chinese reverse analysis plus an English final prompt, Avoid / Do not include, confidence labels, and self-check.

Never:

- Merge multiple images into one prompt.
- Reorder images by content, similarity, quality, or importance.
- Call image-2 or any image generation/editing tool.
- Generate, render, edit, retouch, upscale, cut out, or replace image backgrounds.
- Claim to know the original prompt, real camera body, real lens model, real location, real identity, or exact exposure values without evidence.
- Turn low-confidence details into absolute facts.
- Write uncertainty phrases such as `probably`, `maybe`, `looks like`, `approximately`, or `visually estimated` in the final English prompt.
- Use prompt jargon that forces image-2 to guess the subject, pose, composition, light, or scene relationship.

## Required Workflow

1. Inventory the images before analysis.
   - Count every image the user supplied or referenced.
   - Assign stable labels in upload order: Image 1, Image 2, and so on.
   - If the image order is unclear, state the assumed order before writing prompts.
   - If no image is available, ask the user to upload or provide the image.

2. Analyze each image independently.
   - Do not borrow details from other images unless the user explicitly asks for a combined style.
   - For each image, complete the five layers:
     1. Objective visible image analysis.
     2. Micro-detail reverse analysis.
     3. Photography, composition, and camera-parameter finalization.
     4. image-2 generation-logic reverse analysis.
     5. Final copy-ready deterministic image-2 prompt.

3. Load references only as needed.
   - Read `references/visual-analysis-checklists.md` when deciding what to inspect in the image.
   - Read `references/image2-prompt-rules.md` before drafting or revising the final English prompt.
   - Read `references/camera-parameter-finalization.md` before writing focal length, aperture, shutter, ISO, exposure, white balance, or filter/post-processing in the final prompt.
   - Read `references/output-template.md` when the user did not specify a custom format.
   - Read `references/avoid-do-not-include-guide.md` before writing image-specific Avoid / Do not include lists.
   - Read `references/quality-and-exceptions.md` before final delivery or when images are blurry, partial, ambiguous, or numerous.
   - Read `references/test-checklist.md` when checking the skill itself or forward-testing behavior.

4. Write the output image by image.
   - Start each section with the Chinese heading shown in `references/output-template.md`, equivalent to `Image X -> image-2 reverse prompt X`.
   - Include a separate Avoid / Do not include list for each image.
   - Include confidence labels for high, medium, and low confidence observations.
   - Include the self-check for each image or a final consolidated self-check if the user asks for a compact output.

## image-2 Prompt Priority

Order the final English prompt by generation importance:

1. Subject and scene.
2. Action, body posture, and relaxed or tense body language.
3. Head angle, face direction, expression, gaze direction, iris/eye detail when visible, lips, brows, and skin texture.
4. Hair, hands, body weight, clothing, folds, and material behavior.
5. Composition, aspect ratio, subject placement, subject scale, crop, negative space, visual center, foreground/midground/background relationship.
6. Camera angle, camera height, shooting distance, finalized focal-length look, finalized aperture/depth of field, shutter/subject sharpness, ISO/noise, exposure, white balance, filter or post-processing treatment.
7. Lighting direction, light quality, shadow relationship, color palette, materials, style, atmosphere, realism, and image quality.

Use camera values as finalized generation parameters:

- In analysis, say when focal length, aperture, shutter, ISO, filter, or white balance are uncertain.
- In the final prompt, choose safe deterministic wording such as `Use a 50mm portrait lens look`, `Use f/2.0 shallow depth of field`, `Use a shutter fast enough to keep the subject sharp`, or `Use subtle film-like color treatment`.
- Do not write `visually estimated`, `around`, `approximately`, `possibly`, or similar uncertainty words in the final prompt.
- Do not claim real camera facts unless the user provides them.

## Visibility And Confidence

Use direct wording only for clear visual facts. Use conservative wording for partial or uncertain details:

- Clear: `deep brown eyes`, `direct eye contact`, `centered vertical portrait`.
- Partial: `dark natural eyes with iris color not clearly emphasized`, `the gaze appears slightly off-camera`.
- Unclear in analysis: `eye focus level is not clearly visible`, `camera settings can only be inferred visually`.

For unclear details, choose safe final-prompt wording instead of writing the uncertainty. For real people, describe visible appearance, pose, clothing, and expression. Do not identify the person or infer private attributes.

## Default Output Shape

If the user does not specify a format, use the template in `references/output-template.md`.

Keep the final English prompt copy-ready:

- One coherent paragraph is preferred.
- Avoid bullet-only keyword lists.
- Avoid contradictory style instructions.
- Include only image-relevant details.
- Include uncertainty inside the analysis and confidence sections; keep the final prompt deterministic, executable, and conservative.
