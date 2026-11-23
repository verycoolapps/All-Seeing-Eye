# Rendering Intelligence

## Purpose
Diagnose render quality — photorealism, lighting integration, material response, post-processing, and the specific artifacts that separate "CG" from "photograph."

## Core knowledge
- **Render types:** photorealistic (PBR, path tracing), stylized (toon, painterly), technical (clay/white model), real-time (game engine). Each has different quality criteria.
- **PBR fundamentals:** base color (albedo), metallic (0-1), roughness (0-1), normal map, AO; energy conservation (no surface emits more light than it receives); correct IOR for glass.
- **Lighting in renders:** HDRI/environment lighting vs. practical lights; sun position consistency (shadows must match); color temperature (warm sun + cool fill = natural); bounce light (colored surfaces tint nearby areas).
- **Common render tells:** perfectly clean surfaces (no dust/scratches/wear), unrealistically sharp shadows (area lights too small), missing contact shadows/AO at object bases, floating objects (no ground contact), uniform roughness (everything same gloss), plastic skin (SSS missing or wrong).
- **Post-processing:** bloom (overdone = cheap), vignette (subtle OK, heavy = Instagram filter), chromatic aberration (overdone = distraction), depth of field (too strong = miniature effect), color grading (must serve mood not mask problems).
- **Geometry artifacts:** z-fighting (coplanar surfaces), light leaking (unwatertight mesh), normals flipped (dark patches), UV stretching (texture smear), LOD popping (visible in animation).
- **Camera realism:** focal length (24mm wide vs. 85mm portrait), depth of field (aperture simulation), sensor size; phone-camera characteristics (computational sharpening, HDR processing).

## Evaluation criteria / rules
- Evaluate renders in order: lighting plausibility → material realism → geometry cleanliness → post-processing restraint → camera realism → overall "photograph test."
- The "squint test": blur the image mentally; if the value structure holds, composition is sound; if it collapses, fix values first.
- Check every shadow has a source and every highlight has a reason; floating light = error.
- Materials must show imperfection: wood has grain variation, metal has micro-scratches, fabric has weave texture, skin has pores.
- Flag "too perfect" renders: identical repeated elements, zero wear, symmetrical lighting, no environmental storytelling.
- Compare against reference photos of real materials/lighting when possible.

## Confidence & limits
- High confidence: technical artifacts (z-fighting, flipped normals, missing AO), lighting inconsistencies (shadow direction vs. sun), material impossibilities (mirror-smooth wood).
- Medium: "looks CG," "feels sterile," style appropriateness for the render type.
- Cannot assert: exact render engine settings, whether imperfections are intentional art direction, performance metrics.
- Always ask: is this meant to be photoreal or stylized? Criteria differ completely.
