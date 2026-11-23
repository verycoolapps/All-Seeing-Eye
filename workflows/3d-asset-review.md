# 3D Asset Review

## When to use
Use when reviewing 3D models, game assets, CAD objects, scan results, or asset-store items — mesh quality, topology, UVs, materials, and presentation matter here, often alongside in-engine or viewport screenshots.

## Inputs required
- One or more images of the asset (renders, viewport screenshots, turntable views)
- Optional: file format/pipeline info, target engine (Unity/Unreal/Godot/Blender/CAD), intended LOD/polygon budget
- Optional: close-up detail views if available

## Steps
1. **Identify asset type and target.** Character, prop, environment piece, vehicle, architectural element, scan. Each has different quality bars (characters need anatomy/deformation; props need silhouette and material; environment needs tiling and scale).
2. **Silhouette first.** The most important read: does the outline read correctly at intended viewing distance? Flag unreadable shapes, broken proportions, and details that disappear or overwhelm at target scale.
3. **Topology quality** (from views + knowledge): visible artifacts like pinching, stretching, pole clustering, non-manifold edges showing as shading errors, inconsistent polygon density.
4. **UV/material check.** Texture stretching, seam visibility, texel density consistency, normal map correctness (inverted normals, too-strong normals), missing or placeholder textures, wrong texture scale.
5. **Scale and proportion.** Does the asset match real-world or engine-expected dimensions? Flag assets that are 10x or 0.1x off.
6. **Presentation state.** Is the asset shown with proper lighting, neutral background, multiple angles? Judge the presentation quality itself — bad presentation can hide good assets and vice versa.
7. **Optimization signals.** Visible polycount waste (micro-detail that will never render), unnecessary subdivision, materials count, draw-call implications if instanced.
8. **Score all dimensions** — for assets, Functional Quality (does it serve its purpose in-engine?) and Technical Quality dimensions weighted highest.

## Output format
```
ASSET: <type + intended use>
SILHOUETTE: <assessment>
TOPOLOGY: <assessment or N/A from imagery>
UV/MATERIALS: <assessment>
SCALE: <assessment>
PRESENTATION: <assessment>
ISSUES BY SEVERITY: <blocking / major / minor>
VERDICT: <production-ready / needs work / reject>
```

## Confidence handling
- HIGH: multiple clean views (front/side/iso), neutral lighting, resolution sufficient to judge detail.
- MEDIUM: single view or stylized presentation — mark topology and UV as partially assessable.
- LOW: only in-scene screenshots with heavy post-processing or the asset partially occluded — restrict to silhouette and color/material read; mark technical quality as not assessable.
