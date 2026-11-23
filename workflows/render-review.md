# Render Review

## When to use
Use when reviewing computer-generated imagery — archviz stills, product renders, game screenshots, visualization outputs — where technical rendering quality is part of the evaluation.

## Inputs required
- One or more render images
- Optional: intended use (presentation, marketing, real-estate listing, technical approval), target realism level (photoreal, stylized, diagrammatic)
- Optional: render settings or software info if available

## Steps
1. **Identify render type and target realism.** Photoreal archviz, stylized product shot, diagrammatic, or game-engine capture. The bar differs: photoreal must survive scrutiny; stylized must be internally consistent.
2. **Photorealism audit** (if photoreal target). Hunt for telltale CG artifacts: impossible reflections, uniform noise-free surfaces, over-clean geometry, wrong caustics, floating objects, repeated textures, warped text, melted edges, over-saturated or flat colors, people with plastic skin.
3. **Lighting correctness.** Light sources must be physically plausible: consistent shadow direction/softness, believable bounce light, correct exposure distribution, no light leaking through geometry, emissive surfaces behaving sanely.
4. **Material fidelity.** Each material should show appropriate roughness, texture scale, normal detail, and response to light. Flag default-gray materials, stretched UVs, missing bump/normal detail at close range.
5. **Composition and camera.** Judge like a photograph: rule-of-thirds use, lens distortion realism, depth of field appropriateness, horizon levelness.
6. **Geometry and scene completeness.** Check for unfinished areas, placeholder objects, missing entourage (people, plants, cars) that would ground the scene, or excessive entourage that distracts.
7. **Color grading and post.** Assess whether grading is consistent and purposeful vs. a filter slapped on; check white balance coherence.
8. **Score all dimensions** — weight Functional Quality (does it communicate the design?) and Stylistic Consistency heavily for renders.

## Output format
```
RENDER TYPE: <photoreal/stylized/etc>
REALISM TARGET: <met / partially / missed>
ARTIFACTS FOUND: <list with locations>
LIGHTING: <assessment>
MATERIALS: <assessment>
COMPOSITION: <assessment>
SCORE TABLE: <10 dimensions>
RENDER VERDICT: <usable as-is / needs fixes / rerender>
```

## Confidence handling
- HIGH: high-resolution image, clear artifacts or clean, single coherent scene.
- MEDIUM: compressed or small image — some artifact detection limited; state which checks were degraded.
- LOW: image may be a photo rather than render, or AI-generated image — if AI-generated, shift focus to plausibility and intent rather than render-pipeline artifacts; say so explicitly.
