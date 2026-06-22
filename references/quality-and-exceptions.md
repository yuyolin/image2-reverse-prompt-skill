# Quality And Exceptions

Use this before final delivery and whenever an image is ambiguous, blurry, cropped, or part of a large batch.

## Exception Handling

- If an image is blurry, state `第 X 张图片较模糊，以下反推基于可见内容保守分析，但最终 Prompt 会使用安全确定的 image-2 生成指令。`
- If an image cannot be clearly recognized, state `第 X 张图片无法清晰识别，不能进行高置信反推，但可以基于可见主体输出安全、保守、确定的 image-2 Prompt。`
- If iris color, pupil focus, micro-expression, or finger details are not visible, say so in analysis and use conservative final prompt wording.
- If camera parameters are not provided, explain uncertainty in analysis, then finalize safe generation parameters in the final prompt.
- If a detail is unclear, do not write `unclear` or `not clearly visible` inside the final prompt. Choose safe wording instead.
- If composition is partially visible, still describe subject placement, crop, visual center, and camera angle from the visible frame.
- If many images are supplied, batch output is allowed, but numbering must stay continuous and no image may be skipped.
- If the user uploads images without a text request, default to sequential image-2 reverse prompting.
- If the user requests bilingual output, provide Chinese analysis and English prompts unless they specify otherwise.
- If text, logos, or brands appear, describe visible text/logo placement only when relevant. Do not infer hidden brand meaning or guarantee exact text recreation.

## Final Self-Check

Before answering, verify:

- Image count equals prompt count.
- Image order matches upload order.
- Every image has independent objective analysis.
- Every image has independent micro-detail reverse analysis when relevant.
- Every image has independent composition and camera analysis.
- Every image has independent image-2 generation logic.
- Every image has an independent final English prompt.
- Every image has an image-specific Avoid / Do not include list.
- No images are merged, skipped, duplicated, or mismatched.
- The final prompt is a generation instruction, not an ordinary caption.
- The final prompt uses clear natural language instead of scattered keywords.
- The final prompt follows image-2-friendly priority order.
- The final prompt has no uncertainty phrases such as `probably`, `maybe`, `looks like`, `approximately`, `around`, or `visually estimated`.
- The final prompt uses finalized camera parameters instead of analysis uncertainty.
- Human micro-details cover action, body relaxation, head angle, expression, gaze, eyes, hands, and posture when visible.
- Composition is specific, not generic.
- Camera angle and finalized focal length, aperture, shutter, ISO, exposure, white balance, and filter/post-processing are included when useful.
- Low-confidence details are not written as facts.
- Uncertainty is clearly labeled.
- Output formatting makes each image-to-prompt mapping obvious.

## Confidence Labels

- 高置信: clear, directly visible, safe to include in the final prompt.
- 中置信: supported by visual evidence but should be phrased conservatively in analysis and safely finalized in the prompt.
- 低置信: weakly visible or inferred; keep in analysis only unless a broad safe final-prompt choice is needed.

## Safe Final Wording

- 看不清瞳孔颜色: use `dark natural eyes`.
- 看不清焦距: use `a 50mm portrait lens look` for portraits or `a 35mm documentary lens look` for environments.
- 看不清光圈: use `f/2.0 shallow depth of field` for portraits or `balanced depth of field` for non-portrait scenes.
- 看不清滤镜: use `subtle film-like color treatment` or `clean digital color grading`, whichever better matches the image.
