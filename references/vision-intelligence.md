# Vision Intelligence

## Purpose
Teach the agent to perceive images with structured attention — extracting facts before opinions, and grounding every aesthetic judgment in observable features rather than vibes.

## Core knowledge
- **Feature hierarchy:** color/temperature → value/light distribution → texture/material → edges/lines → composition/layout → objects/semantics → mood/narrative.
- **Global before local:** first pass reads the whole image (light direction, dominant colors, layout grid, focal point); second pass zooms on regions of interest.
- **Depth cues:** perspective convergence, occlusion, relative size, atmospheric haze, defocus. In 3D renders and photos alike, near objects should sit visually "in front."
- **Lighting analysis:** identify source count and direction, shadow softness (crisp = small/hard source; soft = large/diffused), highlight specularity, color of light (warm/cool, high/low saturation), ambient fill level.
- **Scale estimation:** humans (door ~210cm, stair riser ~17-19cm, ceiling residential 240-300cm), car proportions, foliage density relative to architecture.
- **Semantic grounding:** classify scene type (interior/exterior/portrait/still-life/landscape), count objects, note what is present and conspicuously absent (e.g., no people in a living room).
- **Artifact detection:** compression noise, chromatic aberration, banding in gradients, oversharpening halos, upscaling artifacts, render aliasing, missing reflections, z-fighting.
- **Anomaly spotting:** floating objects, impossible shadows, mirrored/duplicated elements, implausible material transitions, physics violations.

## Evaluation criteria / rules
- Always describe WHAT is seen before WHAT it means. "Warm light from upper-left with long soft shadows" precedes "cozy mood."
- Never invent objects that are ambiguous; state ambiguity explicitly ("a small dark shape left of center could be a chair or a plant — unclear at this resolution").
- For edits: diff the image against its intended target; list specific regions, not "looks better/worse."
- Flag resolution limits: below ~512px per side, fine detail claims are unreliable.
- Cross-check perceived facts for internal consistency (e.g., shadows must agree with claimed light direction).

## Confidence & limits
- High confidence: dominant color, broad lighting direction, obvious composition, clear artifacts.
- Medium: material type, mood, style classification, object count in clutter.
- Low/should not assert: exact measurements, hidden-object identities, causality ("the designer intended…"), anything requiring taste alone.
- Never claim pixel-level facts (hex codes, exact dimensions) unless the image metadata or tool provides them.
