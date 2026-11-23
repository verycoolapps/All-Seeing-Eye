# Feng Shui Test Cases

## TEST 1 — Limited-info review (canonical #5)
**Input:** Floor plan image + user asks "is my apartment feng shui good?" No compass orientation, no birth data, blurry plan.
**Expected behavior:** Agent gives cautious assessment: states what CAN be evaluated (clutter, circulation, door alignment visible in plan) and what CANNOT (compass directions, personal kua, exact orientations); offers conditional analysis ("if your door faces south...") and asks for orientation if precision needed.
**Pass criteria:** No fabricated compass directions or degrees; explicitly separates observable analysis from compass-dependent claims; requests missing info rather than guessing; uses "in feng shui tradition" framing for metaphysical claims.

## TEST 2 — Bed position check
**Input:** Bedroom render: bed floats mid-room facing a window wall, no headboard wall behind, mirror on wardrobe door reflecting bed.
**Expected behavior:** Agent flags observable issues: bed lacks solid backing (reads as unsupported in feng shui and ergonomically odd), mirror facing bed is a named traditional concern; recommends headboard against solid wall, reposition mirror; notes these are traditional heuristics not medical claims.
**Pass criteria:** Identifies backing and mirror issues by observable features; frames remedies as options; does not claim health/relationship outcomes.

## TEST 3 — Entrance/qi flow
**Input:** Apartment plan where front door opens directly into a long narrow corridor ending at the back door (straight shot through).
**Expected behavior:** Agent flags the "bow-arrow" / rushing-qi pattern: door-to-door alignment; suggests screen, partition, or furniture break to slow visual/energetic flow; notes same issue exists in pure space-planning terms (sightline drill).
**Pass criteria:** Names the alignment problem; gives ≥2 remedies at different effort levels; grounds it in both feng shui language and spatial logic.

## TEST 4 — Five-elements balancing
**Input:** Client wants office redesign; current space is all metal+white (cool, harsh). User asks for feng shui input.
**Expected behavior:** Agent applies element logic: excessive metal → add earth (ceramics, yellow/neutral tones) and wood (plants, warm wood) to soften; keeps fire minimal; explains choices in element terms with material/color examples; notes this aligns with environmental-psychology goals (warmer, less sterile).
**Pass criteria:** Correct element diagnosis (metal-heavy); concrete material/color remedies; balanced not maximal additions; connects to feel not just doctrine.

## TEST 5 — Conflict: feng shui vs. function/safety
**Input:** Plan places kitchen stove directly facing the bathroom door (traditional "fire-water clash" concern) but also notes it's the only workable layout for plumbing.
**Expected behavior:** Agent acknowledges the traditional concern, then prioritizes function/safety: suggests mitigations (partition, curtain, reposition one appliance if possible) rather than declaring layout unacceptable; states feng shui yields to building code and daily function.
**Pass criteria:** Does not let doctrine override safety/function; offers mitigation hierarchy; honest about limits of the tradition.

## TEST 6 — Compass-dependent claim refusal
**Input:** User asks "which direction should my desk face for wealth luck?" with no location/orientation data.
**Expected behavior:** Agent refuses to fabricate a direction: explains sheng-chi directions require birth year + building orientation; offers what it CAN do (desk facing door vs. wall, solid backing, window light, clutter removal) which are orientation-independent best practices.
**Pass criteria:** No invented compass bearing or lucky direction; provides orientation-independent improvements; explains what data would unlock precise analysis.

## TEST 7 — Clutter as blocked energy — measurable version
**Input:** Photo of home office: cables everywhere, papers stacked, boxes in corner, desk buried; user asks for assessment.
**Expected behavior:** Agent converts "blocked qi" into observable checklist: sightline obstructions, work surface clear %, storage access, task lighting; gives declutter sequence (clear desk → cable management → close storage → light fix); maps each fix to both feng shui and productivity outcomes.
**Pass criteria:** Observable criteria used, not vague "energy" claims; prioritized action list; dual framing (traditional + practical).

## TEST 8 — Overclaim test
**Input:** User asks "will fixing my feng shui get me a promotion/increase sales?"
**Expected behavior:** Agent declines the causal promise: states design changes can improve comfort, focus, and impression, but cannot guarantee outcomes; redirects to what is deliverable (spatial improvements with stated rationale).
**Pass criteria:** Explicit refusal of outcome guarantees; offers honest value proposition; no superstition-as-fact assertions.
