# Product identity and action completion

Use this reference for multiple product images, labels repeated across different packages, or a repeated action that stops before completion.

## Reference mapping

Bind each product reference to three things: its image ID, exact product name when known, and scene/time interval. Example for a five-product, 15-second sequence:

| Reference | Product | Interval |
|---|---|---|
| Image 1 | Exact brand and fragrance name from reference 1 | 0–3 seconds |
| Image 2 | Exact brand and fragrance name from reference 2 | 3–6 seconds |
| Image 3 | Exact brand and fragrance name from reference 3 | 6–9 seconds |
| Image 4 | Exact brand and fragrance name from reference 4 | 9–12 seconds |
| Image 5 | Exact brand and fragrance name from reference 5 | 12–15 seconds |

Replace the product-name descriptions with verified names when known. Never invent a brand to fill a missing name. Add a portrait as a separately identified person reference only if the intended shot requires it.

## Reusable identity wording

> These references represent different products. Treat each product as a separate complete identity. Preserve its reference shape, proportions, materials, colour, cap, original label layout, logo, brand name, and product name together. The label belongs exclusively to its corresponding reference product. Never transfer a name, logo, or label to another product, merge the references, or create variations of Product 1. Preserve each product's identity during its entire assigned scene, including handling.

This wording expresses desired fidelity. It does not prove that a model will reproduce small printed text exactly.

## Reusable pickup wording

> Show the required number of completed pickups. Each pickup visibly includes gripping the product, lifting its base clear of the supporting surface, and pulling the entire product outside its container. Show the original position empty. Touching or gripping a product while it remains supported does not complete the pickup. In the final scene, finish the extraction before holding the product for the closing shot.

Use completion conditions appropriate to the actual action; do not apply pickup rules to unrelated movements.

## Bathroom-perfume case

Concept: the same person opens an opaque bathroom cabinet each morning, takes out a different perfume, and closes the door. The closed door conceals the time skip. Camera and room remain fixed.

The initial prompt described five generic bottle designs and requested small, simple front labels rather than explicitly preserving each reference's branding. In a reviewed 15-second result, the first four pickups completed; the fifth hand gripped a bottle that remained on the shelf. The user identified the principal issue as one fragrance name recurring on four of five bottles while their forms varied. Exact product-name matches could not be independently checked without the five product references.

These are distinct problems:

- **Product identity:** explicitly bind each original package and label to its reference and interval; remove instructions to simplify original labels.
- **Action completion:** require full extraction and an empty shelf before the final hold. Define an end state visibly different from a bottle still resting on the shelf.

A possible final-scene revision for this specific 15-second setup:

```text
12.0–12.7 seconds: Open the cabinet to reveal Perfume 5 from its assigned reference.
12.7–13.2 seconds: Grip Perfume 5 around its sides, keeping the fragrance name visible.
13.2–13.8 seconds: Lift its base clearly off the shelf, then pull the entire bottle forward outside the cabinet frame.
13.8–15.0 seconds: Hold it upright outside the cabinet, with its original label facing the camera. Keep its empty shelf position visible behind it.
```

This revision is untested in a new generation. Adapt duration and movement speed to the actual brief.

## If fidelity still fails

Offer separate clips with one product reference per clip and matched scene framing. Join them at the fully closed door, or at the user's chosen concealment event. This reduces cross-product ambiguity but still requires inspection of labels and geometry.

For exact packaging text, offer compositing with verified original product imagery. Keep generated footage and source assets separate until the user requests an edit; prompt troubleshooting alone is not an instruction to generate, edit, or publish a video.
