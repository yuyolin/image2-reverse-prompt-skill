# Test Checklist

Use this checklist when validating the skill or forward-testing it on sample image requests.

- Single portrait image produces exactly one image-2 prompt.
- Multiple images preserve original upload order.
- Multiple similar images are not merged.
- Blurry images are handled conservatively.
- Unrecognizable images do not trigger invented subjects.
- Invisible iris color is not fabricated.
- Low-confidence micro-expression details stay in analysis or become safe final wording.
- Hands and fingers are analyzed when visible.
- Complex composition is described specifically, not with generic labels.
- Camera angle, camera height, and shooting distance are handled.
- Focal length, aperture, shutter, ISO, exposure, white balance, and filter/post-processing are finalized as generation parameters.
- Final prompt contains no uncertainty phrases such as `probably`, `maybe`, `looks like`, `approximately`, `around`, or `visually estimated`.
- Final prompt is complete English natural language, not keyword stuffing.
- Avoid / Do not include is tailored to the image type.
- Each image has its own confidence labels.
- Each image has its own self-check.
- The skill only generates prompts and does not call image generation, edit images, or imply it created an image.
