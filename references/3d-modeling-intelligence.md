# 3D Modeling Intelligence

## Purpose
Guide and critique 3D models, renders, and generated geometry — topology, proportion, detail level, UV/material preparation, and the gap between "looks right" and "is right."

## Core knowledge
- **Topology quality:** quads preferred for subdivision/deformation; triangles acceptable for static hard-surface; n-gons only for flat planes; pole placement (5+ edges meeting) avoided in curved/deforming areas; edge loops follow anatomy/structure.
- **Silhouette first:** a model reads as good/bad primarily through its silhouette; detail only matters if the outline is correct. Check silhouette before texture.
- **Proportion systems:** human ~7.5 heads tall, hands ~face length, feet ~head length; animals on module systems; architecture on grids (meters).
- **Detail hierarchy:** primary forms (big masses) → secondary (major features) → tertiary (surface detail) → quaternary (micro/wear). Don't spend polygons on tertiary if primary is wrong.
- **Bevels and edge treatment:** real-world edges are never razor-sharp; 1-3mm bevels catch light and sell realism; zero-radius edges look CG.
- **UV and materials:** clean UVs (no stretching, consistent texel density), material zones (wood vs. metal vs. fabric separate), PBR workflow (base color, metallic, roughness, normal).
- **Common modeling failures:** melted/intersecting geometry, inverted normals, non-manifold edges, floating parts, symmetric perfection (humans are asymmetric), uniform bevels everywhere.
- **Render-readiness:** scale correctness (meters not centimeters), origin/pivot placement, naming conventions, LOD strategy for games.

## Evaluation criteria / rules
- Evaluate models in order: silhouette → proportion → topology → surface detail → materials → technical cleanliness.
- For generated models: check if it's "game-ready" (low poly + textures), "film-ready" (high poly + displacement), or "print-ready" (watertight, correct scale).
- Flag "AI-generated look": over-smoothed surfaces, impossible geometry, uniform detail density, missing wear/imperfection.
- When critiquing topology, specify WHERE ("pole at elbow," "ngons on curved surface") not just "bad topology."
- For humanoid models, always check: head-body ratio, shoulder width, limb lengths, hand/feet structure, pose plausibility.
- Recommend fixes proportionally: retopo > fix proportions > add detail > adjust materials.

## Confidence & limits
- High confidence: topology errors visible in wireframe/close-up, proportion breaks, obvious intersections, scale errors.
- Medium: "too high-poly," "needs more detail," style appropriateness.
- Cannot assert: exact polygon counts for a specific engine without specs, print-ability without wall-thickness data, animation-deformation quality without rig.
- Always distinguish visual quality (render) from technical quality (topology/data) — a pretty render can hide bad topology.
