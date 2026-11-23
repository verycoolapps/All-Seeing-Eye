# Rendering Test Cases

## TEST 1 — Beautiful render with unrealistic lighting (canonical #1, render-specific)
**Input:** Archviz interior, gorgeous materials, but lit by three overlapping HDRIs plus four practicals with no logic — shadows contradict each other, ambient is flat.
**Expected behavior:** Agent flags lighting as physically incoherent: lists shadow-direction conflicts, unmotivated sources, flat ambient; notes this breaks photorealism regardless of material quality.
**Pass criteria:** ≥2 specific lighting contradictions named; explains why it reads "CG" despite good assets; distinguishes asset quality from scene lighting quality.

## TEST 2 — Plastic-looking wood material (render-specific)
**Input:** Oak parquet floor in render: single albedo color, roughness map uniform at 0.4, no normal map, no grain depth under raking light.
**Expected behavior:** Agent diagnoses missing PBR maps: needs albedo variation, roughness breakup (0.3-0.6 range), normal/height for grain; explains that lighting angle reveals the fake.
**Pass criteria:** Names specific missing/incorrect maps; links visual symptom ("looks like laminate/plastic") to technical cause; suggests map set.

## TEST 3 — Contact-shadow / floating objects
**Input:** Product render of a chair on a floor: chair legs end abruptly, no AO gradient beneath, soft shadow 30cm away from leg base.
**Expected behavior:** Agent identifies missing contact shadows/AO: objects appear to hover; prescribes AO pass, tighter shadow mapping, or ground-plane fix.
**Pass criteria:** Names the grounding failure; explains physical cause; suggests technical fix (AO, shadow settings).

## TEST 4 — Z-fighting / intersecting geometry
**Input:** Close-up render where two wall panels show flickering striped overlap pattern and a decal appears to swim across the surface.
**Expected behavior:** Agent identifies z-fighting (coplanar faces) and/or decal projection issues; explains cause (overlapping geometry at same depth) and fix (offset surfaces, polygon offset).
**Pass criteria:** Correctly names z-fighting; explains mechanism; suggests concrete fix; distinguishes from texture artifact.

## TEST 5 — Post-processing overreach
**Input:** Photo-real render with heavy bloom on every light, strong vignette, chromatic aberration at edges, and crushed-black shadows "for mood."
**Expected behavior:** Agent flags each effect as excessive and masking underlying issues: bloom hiding blown highlights, vignette narrowing composition artificially, aberration distracting, crushed blacks losing material detail; recommends dialing back to reveal base render quality.
**Pass criteria:** Lists ≥3 specific post-processing problems; explains what each hides or damages; advises evaluating pre-post image.

## TEST 6 — Camera/lens realism
**Input:** "Photoreal" interior shot with 14mm-equivalent perspective (walls converging dramatically), infinite depth of field, and phone-photo sharpening halos.
**Expected behavior:** Agent notes lens-character problems: ultra-wide distortion inappropriate for the genre, deep DOF reads as CGI not photo, sharpening halos reveal upscaling/denoise; recommends 24-35mm for interiors and appropriate aperture.
**Pass criteria:** Identifies lens/DOF mismatch with genre; explains why it breaks photorealism; suggests appropriate focal length/aperture.

## TEST 7 — Uncanny skin/material in character render
**Input:** Human character render with waxy uniform skin, no pores or subsurface variation, hair as solid helmet mesh, eyes with perfect catchlights but dead gaze.
**Expected behavior:** Agent flags uncanny-valley cluster: missing SSS/texture variation in skin, hair lacking strand detail, eyes lacking moisture/life; notes combination triggers revulsion more than any single flaw.
**Pass criteria:** Names ≥3 uncanny cues; explains synergistic effect; prioritizes fixes (skin SSS first, then eyes, then hair).

## TEST 8 — Render vs. photo comparison (canonical #9 adjacent)
**Input:** Side-by-side: real photo of a café interior vs. Archviz render of same space.
**Expected behavior:** Agent compares systematically: real photo has light falloff, material wear, lived-in clutter, imperfect white balance; render is cleaner, more contrasty, geometrically perfect; identifies specific gaps (missing wear, lighting logic, human traces) that keep render from passing as photo.
**Pass criteria:** Dimension-by-dimension comparison; ≥3 specific realism gaps; acknowledges what render does BETTER (composition, cleanliness) for balance.
