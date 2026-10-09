# Reusable prompt template

Replace bracketed fields with concrete choices before returning a final prompt. Omit inapplicable detail while keeping the seven sections distinct.

```text
Create a [visual style] [duration]-second [aspect ratio] video featuring [subject count and description], using [reference images/assets] in [specified order].

IDENTITY AND REFERENCES:
Preserve [identity, face, proportions, hairstyle, product geometry, or other essential features].
Reference 1 supplies [appearance/state 1], continuing through [final appearance/state].
For referenced products, map each [image ID] to [exact brand/product name, when known] and [scene/time interval]. Keep any person reference separate from this product sequence.
Reproduce [required clothing, materials, colours, accessories, or product details] accurately.
For each branded product, preserve its own [shape, proportions, material, colour, cap, original label, logo, brand, and product name] together. Do not copy labels or names between products, merge references, or redesign the packaging.
Use the references for [identity/appearance]; recreate the setting and actions below.

CAMERA AND COMPOSITION:
Use [precise camera position, optical-axis direction, shot size, and framing].
[Specify whether the camera is stationary or follows a defined movement.]
Place [subject] at [screen position] within [environment].
Maintain [body/product scale, orientation, and framing boundaries].
Specify the moving elements: [subject/object]. Specify the stationary elements: [background/camera, if applicable].

MAIN VISUAL MECHANISM:
[Object or physical event] creates the transitions.
Describe its [material, shape, scale, position, direction, speed, and interaction with the subject].
Its movement is independent of [stationary camera/environment, where applicable].

TIMING AND ACTION:
[Time range]: Opening action establishing [subject and initial appearance].
[Time range]: Subject performs [trigger action].
[Time range]: Transition mechanism begins moving.
[Time range]: Designated transition reveals [next appearance and pose].
[Repeat with explicit timing for every intended reveal.]
[For each essential action]: Show [starting state] → [physical action] → [observable completed state].
[Final time range]: Reveal [final appearance], complete [required final action], then hold it clearly until the end.

TRANSITION RULES:
Exactly [number] appearances and [number] changes.
Exactly [number] completed [required actions], verified by [visible completion condition]. Merely showing or touching a product does not complete its required action.
Each change occurs only during [designated concealment event].
Define how the previous appearance disappears and the new appearance becomes visible.
Any other passes of the transition object leave the appearance unchanged.
Specify whether pose changes happen through continuous movement or complete concealment.
No [unwanted morphing, dissolves, flashes, or exposed cuts].

CONTINUITY AND QUALITY:
Maintain consistent [identity, camera, environment, scale, position, lighting, and shadows].
Keep each referenced product and its own branding consistent throughout its assigned scene and handling. Keep fingers clear of [important label text] when it must be visible.
Use believable [anatomy, movement, materials, and physical interactions].
Exclude [scene-specific unwanted artifacts].
```
