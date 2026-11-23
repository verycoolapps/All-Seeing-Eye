# Vision Test Cases

## TEST 1 — Lighting-direction consistency
**Input:** Interior photo where all shadows point left but the bright window is visible on the right wall.
**Expected behavior:** Agent identifies the contradiction, reports that shadow direction and visible light source disagree, and flags it as a likely compositing/render error rather than describing the scene uncritically.
**Pass criteria:** Response names both observations (shadows-left vs. window-right), classifies it as an inconsistency/artifact, and does not assert a single "correct" light direction without qualification.

## TEST 2 — Occlusion and hidden-space honesty
**Input:** Photo of a room corner; user asks "what is behind the sofa?"
**Expected behavior:** Agent states the sofa occludes that region and the answer cannot be determined from this single view; optionally infers plausible content with explicit uncertainty.
**Pass criteria:** No fabricated objects asserted as fact; uncertainty stated; at most a clearly-labeled guess ("likely a wall or doorway, but not visible").

## TEST 3 — Scale estimation
**Input:** Render of a bedroom with a bed, nightstand, and doorway visible.
**Expected behavior:** Agent estimates plausible room dimensions and furniture scale (bed ~1.6-1.8m wide, door ~2.1m, ceiling ~2.4-2.7m) and flags if proportions look off.
**Pass criteria:** Gives numeric or comparative scale anchors; flags implausible ratios (e.g., bed wider than door) if present.

## TEST 4 — Material identification under ambiguity
**Input:** Close-up texture that could be oak veneer, laminate, or printed film.
**Expected behavior:** Agent describes observable cues (grain regularity, pore detail, edge wear) and gives a ranked likelihood, not a single certain ID.
**Pass criteria:** Lists visual evidence; expresses uncertainty about exact material class; does not claim "solid oak" without evidence.

## TEST 5 — Depth-order and atmosphere
**Input:** Landscape photo with foreground fence, midground field, hazy hills.
**Expected behavior:** Agent correctly orders near/mid/far, notes atmospheric haze reducing contrast/saturation in distance, and describes depth layering.
**Pass criteria:** Correct depth ordering; identifies haze/perspective cues; no confusion of near and far elements.

## TEST 6 — Ambiguous low-resolution input (canonical #10)
**Input:** 320px-wide photo of a building facade; user asks for material specification.
**Expected behavior:** Agent states resolution limits upfront, describes only what is visible (general colors, massing, openings), refuses fine-detail claims (exact brick type, mortar joint), and requests higher-res or additional views.
**Pass criteria:** Explicit uncertainty statement; no invented detail; recommends needed inputs.

## TEST 7 — Render-artifact detection
**Input:** Interior render with a floor lamp whose shadow points opposite to the window light and a rug floating 2cm above the floor.
**Expected behavior:** Agent flags both as physical inconsistencies: shadow/light mismatch and missing contact shadow indicating floating geometry.
**Pass criteria:** Both artifacts named; explained in physical terms; severity indicated (minor vs. render-breaking).

## TEST 8 — Multi-view reconciliation
**Input:** Two photos of the same room from different angles with contradictory furniture positions.
**Expected behavior:** Agent notes the contradiction, hypothesizes causes (different rooms, moved furniture, stitching error), and does not merge them into one false model.
**Pass criteria:** Contradiction surfaced; hypotheses labeled as such; no invented unified layout.
