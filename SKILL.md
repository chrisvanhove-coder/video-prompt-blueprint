---
name: video-prompt-blueprint
description: Write or revise structured AI video prompts with reference-image mapping, explicit camera behavior, timed action, physical reveal transitions, and continuity. Use for reusable fashion, product, and character video prompt design, including unwanted camera movement.
---

# Video Prompt Blueprint

Turn a video concept into a ready-to-use prompt with seven explicit sections. The reference pattern is **opening action → trigger → timed reveals → clear final hold**. Adapt that pattern to the user's concept; the fan, five outfits, male subject, overhead view, and 15-second duration belong to the example, not every video.

This skill authors prompts. Generate, edit, upload, or publish a video only when the user requests that additional action. Do not promise virality or exact model compliance.

## Establish the brief

Use the user's duration, aspect ratio, subjects, references, camera choice, environment, and intended transformation. Preserve explicit creative decisions. Ask only for missing details that materially affect the result; otherwise state reasonable assumptions briefly outside the finished prompt.

Map references by upload order or supplied labels. Distinguish identity references, wardrobe/product references, setting references, and visual-style references. Do not claim to have inspected unavailable images. When only drafting from a described brief, use the supplied descriptions and reference labels.

## Write the seven sections

1. **Output specification.** Define visual style, duration, aspect ratio, subject count, and reference order in the opening sentence.
2. **Identity and references.** Specify what stays consistent and which image supplies each outfit, product state, or appearance. Preserve applicable face, skin tone, physique, hairstyle, garment, material, colour, footwear, and accessory details.
3. **Camera and composition.** Specify camera position, optical-axis direction, framing, screen-space orientation, environment, subject scale, and visible margins. State which objects may move and which remain fixed.
4. **Main visual mechanism.** Describe the transition object/event's material, shape, foreground/background position, direction, speed, and physical interaction. Separate its movement from camera movement.
5. **Timing and action.** Use explicit contiguous time intervals from zero to the requested duration. Each interval identifies the action and the appearance visible before/after any reveal. Give the final appearance enough readable screen time.
6. **Transition rules.** Specify appearance count, change count, designated concealment events, and reveal boundaries. For a linear sequence of N appearances, use N−1 changes unless the user requests a loop or revisiting appearances.
7. **Continuity and quality.** Specify persistent identity, environment, subject scale and position, lighting, shadows, anatomy, and material behavior. Include relevant exclusions rather than an indiscriminate negative-prompt list.

Use [references/prompt-template.md](references/prompt-template.md) for a reusable scaffold. Read [references/chrome-fan-example.md](references/chrome-fan-example.md) when adapting the original five-outfit concept or checking how the sections work together.

## Stationary-camera wording

When the user requests a stationary camera, explicitly anchor the frame:

> Locked-off tripod shot. The camera remains fixed in world space throughout. Keep its position, orientation, focal length, and framing constant. The stationary background stays registered to the same screen coordinates. Only the specified subject and transition object move. No pan, tilt, zoom, dolly, orbit, handheld shake, or automatic reframing.

For a directly overhead shot, say the optical axis points vertically downward, perpendicular to the floor. A floor-parallel sensor plane avoids ambiguous descriptions of a camera angle. Keep meaningful fixed background anchors visible when the composition permits. Do not add tracking, push-ins, cinematic camera motion, or focus instructions that imply reframing.

If camera movement persists, first remove conflicting camera phrases and simplify simultaneous actions while preserving the concept. If the user names a tool with camera settings, use verified available controls. Explain briefly that prompt wording expresses intent and may still require generation settings or a locked-frame compositing workflow; do not claim the wording guarantees a fix.

## Concealed transitions and physical feasibility

- Define the transition spatially: the old appearance remains ahead of the occluder's leading edge; the new appearance is exposed behind its trailing edge. Regions under the occluder are hidden. Avoid exposed clothing morphs, dissolves, flashes, and jump cuts when those violate the brief.
- A rotating fan or repeating object can pass many times. Assign changes to designated passes; all other passes leave the appearance unchanged. Rotation count and outfit-change count are separate constraints.
- An instantaneous pose change needs complete concealment of all body regions that move. With partial concealment, keep the pose fixed during the appearance change or choreograph a natural continuous pose movement between reveals.
- Check the opening composition against the opening action. If the subject starts fully supported on a sofa, that sofa and camera frame must accommodate the entire body. Preserve a deliberate crop only if it remains physically compatible.
- Check occluder scale, depth, rotation timing, subject position, and final visibility. If the intended geometry cannot hide the specified changes, identify the conflict and offer the smallest concrete adjustment. Do not silently replace the user's main mechanism.

## Deliver and review

Deliver one complete usable prompt. Put any assumptions or material feasibility notes outside it. For a narrow revision, preserve unrelated sections and reference mappings.

Before returning it, check timing coverage, reference order, appearance/change counts, camera consistency, concealment coverage, opening support/framing, and readable final hold. Distinguish creative instructions from demonstrated results: the example is an untested prompt, not a verified successful generation.
