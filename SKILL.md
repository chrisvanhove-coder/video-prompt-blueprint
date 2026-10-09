---
name: video-prompt-blueprint
description: Write or revise structured AI video prompts with reference-image mapping, product and label identity, explicit camera behavior, completed timed actions, physical reveal transitions, and continuity. Use for fashion, product, and character prompts or reviewing camera drift, repeated labels, and missed actions.
---

# Video Prompt Blueprint

Turn a video concept into a ready-to-use prompt with seven explicit sections. The reference pattern is **opening action → trigger → timed reveals → clear final hold**. Adapt that pattern to the user's concept; the fan, five outfits, male subject, overhead view, and 15-second duration belong to the example, not every video.

This skill authors prompts. Generate, edit, upload, or publish a video only when the user requests that additional action. Do not promise virality or exact model compliance.

## Establish the brief

Use the user's duration, aspect ratio, subjects, references, camera choice, environment, and intended transformation. Preserve explicit creative decisions. Ask only for missing details that materially affect the result; otherwise state reasonable assumptions briefly outside the finished prompt.

Map references by upload order or supplied labels. Distinguish identity references, wardrobe/product references, setting references, and visual-style references. Do not claim to have inspected unavailable images. When only drafting from a described brief, use the supplied descriptions and reference labels.

For multiple referenced products, make an explicit mapping from each image ID to its product and scene/time interval. Add the exact brand and product name when supplied or clearly readable; ask for an unreadable name when exact text is essential. A person's portrait is a separate identity reference and must not enter the product sequence. Do not replace actual referenced products with invented generic designs unless the user requests redesign.

## Write the seven sections

1. **Output specification.** Define visual style, duration, aspect ratio, subject count, and reference order in the opening sentence.
2. **Identity and references.** Specify what stays consistent and which image supplies each outfit, product state, or appearance. Preserve applicable face, skin tone, physique, hairstyle, garment, material, colour, footwear, and accessory details. For branded products, bind each bottle/package to its own label, logo, brand, and product name.
3. **Camera and composition.** Specify camera position, optical-axis direction, framing, screen-space orientation, environment, subject scale, and visible margins. State which objects may move and which remain fixed.
4. **Main visual mechanism.** Describe the transition object/event's material, shape, foreground/background position, direction, speed, and physical interaction. Separate its movement from camera movement.
5. **Timing and action.** Use explicit contiguous time intervals from zero to the requested duration. Each interval identifies the action and the appearance visible before/after any reveal. Give essential actions observable completion states and sufficient time before a final hold.
6. **Transition rules.** Specify appearance count, change count, designated concealment events, and reveal boundaries. Count required completed actions separately from appearances. For a linear sequence of N appearances, use N−1 changes unless the user requests a loop or revisiting appearances.
7. **Continuity and quality.** Specify persistent identity, environment, subject scale and position, lighting, shadows, anatomy, and material behavior. Include relevant exclusions rather than an indiscriminate negative-prompt list.

Use [references/prompt-template.md](references/prompt-template.md) for a reusable scaffold. Read [references/chrome-fan-example.md](references/chrome-fan-example.md) when adapting the original five-outfit concept or checking how the sections work together.

For multi-product sequences, repeated labels, or incomplete pickups, read [references/product-identity-and-actions.md](references/product-identity-and-actions.md). It includes the bathroom-perfume case; its five products, cabinet, and timing are example-specific.

## Product identity and completed actions

Treat each referenced product as a complete independent identity: shape, proportions, material, colour, cap, label layout, logo, brand, and product name travel together. Explicitly prohibit copying one product's label onto another, merging references, or generating variations of the first product. Preserve that identity on the shelf, in the hand, and through any permitted motion. Label visibility should match the intended product shot and physical orientation.

For original packaging, remove conflicting phrases such as "simple labels," "generic bottle," or "without brand names." Keep fingers clear of the important label text when it must be shown. This is desired behavior, not a guarantee of exact text rendering.

Specify the visible result of an essential action. For extraction: grip → lift clear of the supporting surface → pull fully outside the container. Confirm the original position is empty. A hand touching or gripping a supported object is not a completed pickup. For the last scene, finish the action before settling into the final product hold; a showcase must not replace a required removal.

Check the action budget: opening, gripping, lifting, presenting, exiting, and closing all need time. Simplify optional movements or offer a longer duration when necessary; do not silently change the requested length.

If repeated labels persist, offer separate clips with one product reference per clip, matched backgrounds, and joins concealed by the chosen transition. When exact packaging text is essential, offer an edit using verified original product imagery or label compositing. Do not claim that stronger wording or separate clips guarantees fidelity, and do not execute either fallback unless requested.

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

For product sequences, also check per-scene product/name mapping, label isolation, completed-action counts, and the final scene's completion state.

When reviewing a generated result, inspect the available footage and compare it with the submitted prompt and references. Separate observed failures, user-reported details, and inferred causes. If references or the exact submitted prompt are unavailable, state that limit rather than claiming an identity match. Distinguish action omission from product-identity or label errors; acknowledge and incorporate the user's correction. Proposed prompt fixes remain untested until a new generation is reviewed.
