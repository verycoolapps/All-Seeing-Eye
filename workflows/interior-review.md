# Interior Review

## When to use
Use when reviewing interior spaces — room photos, floor plans with finishes, 3D interior renders, real-estate listing images, or hospitality/commercial interiors needing critique.

## Inputs required
- One or more interior images
- Optional: room type and intended function (kitchen, lobby, bedroom, office), style target, occupant profile
- Optional: plan/layout information if available

## Steps
1. **Identify function and user.** What activity happens here, for whom, under what conditions (lighting, acoustics, privacy)? All subsequent judgments are relative to function.
2. **Spatial layout read.** From imagery: circulation paths, furniture placement logic, entry sequence, sightlines, clustering of activity zones. Flag blocked pathways, dead corners, and furniture fighting the architecture.
3. **Scale and proportion.** Do ceiling heights, furniture sizes, and room dimensions feel coherent? Flag dollhouse-scale errors (oversized sofas in small rooms, undersized lighting).
4. **Lighting analysis.** Identify light sources: natural (window position, time of day guess), artificial (type, warmth, placement). Check for dark corners, glare, color temperature clashes, and missing task lighting.
5. **Material and finish palette.** List the finish palette; assess cohesion, tactile contrast, maintenance realism, and whether materials suit the room's function (e.g., light carpet in a mudroom).
6. **Color and mood.** Evaluate color scheme: harmony, contrast ratio, accent discipline. Does the palette produce the intended mood (calm, energizing, luxurious)?
7. **Detail and styling.** Assess accessories, art, plants, textiles: curated vs. cluttered, scale-appropriate, stylistically consistent.
8. **Score all dimensions** with Functional Quality weighted highest for inhabited spaces; run priority-system on all issues.

## Output format
```
SPACE: <type + function>
LAYOUT: <assessment>
LIGHTING: <assessment>
MATERIALS/COLOR: <assessment>
STYLING: <assessment>
SCORE TABLE: <10 dimensions>
ISSUES BY PRIORITY: <from priority-system>
VERDICT: <rating + one-line summary>
```

## Confidence handling
- HIGH: multiple angles showing full room, daylight visible, function known.
- MEDIUM: single view or wide-angle distortion (fisheye/wide lenses exaggerate space) — correct mentally for distortion and note it.
- LOW: staged/virtual staging without disclosure, or partial views only — mark spatial flow and lighting as partially assessable.
