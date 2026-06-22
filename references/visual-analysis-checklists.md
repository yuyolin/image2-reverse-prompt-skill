# Visual Analysis Checklists

Use these checklists to inspect each image before writing the prompt. Do not force every item into the final answer if it is not visible or relevant.

## Subject And Scene

- Subject type: person, product, interior, architecture, food, landscape, vehicle, animal, abstract object, or mixed scene.
- Apparent age range or visual type when relevant and non-sensitive.
- Subject role: only visual center, one of several centers, background element, or environmental detail.
- Subject state: standing, sitting, moving, resting, posing, interacting, isolated, staged, candid, commercial, documentary.
- Scene type: studio, street, bedroom, apartment, office, restaurant, nature, waterfront, exhibition space, commercial set, minimal background, cinematic environment.
- Scene depth: shallow, layered, compressed, wide environment, blurred background, clear spatial context.

## Human Micro-Details

Use for portraits, fashion, lifestyle, editorial, cosplay, cinematic stills, and any image with visible people.

- Body language: relaxed, tense, stiff, elegant, casual, lazy, controlled, dynamic, compressed, expansive.
- Shoulders and neck: lowered shoulders, tight shoulders, open chest, relaxed neck, elongated neck, hunched posture.
- Body weight: centered, shifted to one leg, leaning forward/backward, hip twist, torso rotation.
- Arms and hands: loose arms, bent elbows, relaxed wrists, curled fingers, stiff fingers, hidden hands, cropped hands, object interaction.
- Head angle: front-facing, profile, three-quarter, turned away, looking over shoulder, lowered chin, raised chin, tilted head, extended neck.
- Face direction versus gaze direction: aligned, looking off-camera, direct eye contact, side glance, downward gaze, upward glance.
- Expression: relaxed lips, slightly parted lips, faint smile, pressed lips, exposed teeth, lowered brows, raised brows, half-lidded eyes, restrained emotion, melancholy, detached, gentle, confident, tired, playful, confrontational.
- Eyes and irises: direct eye contact, unfocused gaze, soft distant gaze, sharp focused gaze, visible iris color, shadowed eyes, iris color not visible.
- Skin and face detail: skin texture, pores, makeup, under-eye shadow, cheekbone shadow, nose highlight, lip moisture, soft focus, retouching, grain.
- Hair: smooth, messy, wind-blown, damp, flyaway strands, face-covering hair, backlit hair edge, cropped hair.
- Clothing: silhouette, fit, fabric folds, wrinkles, transparency, gloss, matte texture, layering, styling mood.

## Non-Human Subject Details

- Product: shape, proportions, surface finish, material, logo/text visibility, reflection, edge sharpness, packaging, scale cues.
- Architecture/interior: symmetry, vertical lines, vanishing point, spatial rhythm, furniture placement, material palette, window/light direction.
- Food: plating, texture, gloss, steam, sauce, crumbs, scale, plate/table material, appetizing freshness.
- Landscape: horizon, foreground/midground/background, weather, terrain, water, sky, atmospheric depth, natural or stylized color.

## Composition

Judge composition from the actual image, not from generic labels.

- Aspect ratio: vertical, horizontal, square, panoramic, cropped social format.
- Shot size: extreme close-up, close-up, medium close-up, waist-up, full body, wide, environmental.
- Subject placement: centered, slightly off-center, thirds, symmetric, diagonal, frame-within-frame, leading lines, negative space.
- Subject scale: percent of frame, headroom, side space, body crop, hands/feet crop.
- Visual center and movement: stable, tense, directional, diagonal pull, top-heavy, bottom-heavy, balanced, intentionally awkward.
- Layering: foreground, midground, background, background separation, depth-of-field isolation.
- Camera position: eye level, low angle, high angle, overhead, tilted, close handheld, distant compressed.

## Camera And Lens Finalization

Analyze these cautiously, then turn them into safe deterministic generation parameters in the final prompt unless actual EXIF/user data is available. Keep uncertainty in analysis and confidence labels.

- Focal-length feel: wide-angle distortion, natural 35mm/50mm feel, compressed 85mm/135mm portrait feel, telephoto compression.
- Aperture/depth of field: deep focus, shallow background blur, subject-background separation, bokeh softness.
- Shutter: sharp frozen subject, slight motion blur, handheld blur, long-exposure trails.
- ISO/noise: clean low-noise look, visible digital noise, film grain, high ISO atmosphere.
- Exposure: low-key, high-key, clipped highlights, crushed shadows, balanced exposure.
- White balance: warm, cool, neutral, green cast, magenta cast, mixed lighting.
- Filter/post tendency: film-like, matte, high contrast, faded blacks, clean digital, HDR, bloom, diffusion, halation.

Final prompt examples:

- Unclear portrait focal length: `Use a 50mm portrait lens look.`
- Strong compression: `Use an 85mm portrait lens look with natural background compression.`
- Shallow portrait blur: `Use f/2.0 shallow depth of field.`
- Sharp subject: `Use a shutter fast enough to keep the subject crisp.`
- Clean image: `Use low ISO with clean shadow detail.`
- Film tone: `Use subtle film-like color treatment.`

## Light, Color, Material, Style, Quality

- Light direction: front, side, back, top, window, practical lamp, neon, sunset, studio softbox, hard flash.
- Light quality: soft, hard, diffused, directional, low contrast, harsh shadows, rim light, specular highlights.
- Color system: muted neutrals, warm beige/brown, cool blue/green, high saturation, monochrome, complementary, pastel, cinematic teal-orange, natural skin tones.
- Materials: skin, fabric, metal, glass, plastic, wood, stone, leather, water, smoke, fog, wet pavement, matte ceramic, glossy finish.
- Style: realistic, cinematic still, editorial fashion, commercial product, documentary street, minimalist lifestyle, clean Korean aesthetic, Japanese natural light, Xiaohongshu lifestyle, luxury magazine, film photography, raw portrait.
- Quality: sharp focus, soft focus, high resolution, natural grain, subtle texture, over-smoothed, compressed, over-sharpened, professional camera look, smartphone look.
