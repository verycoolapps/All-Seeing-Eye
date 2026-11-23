# Architecture Test Cases

## TEST 1 — Structural plausibility check
**Input:** Building render with a 12m cantilevered concrete box, no visible columns or supports, thin slab edge.
**Expected behavior:** Agent flags structural implausibility: cantilever depth-to-thickness ratio unrealistic for concrete; asks about structure or marks as "conceptual, not buildable" unless context says otherwise.
**Pass criteria:** Names the specific structural problem; does not accept render realism as proof of buildability; suggests plausible fixes (columns, deeper section, cable stay).

## TEST 2 — Facade rhythm analysis
**Input:** Apartment facade photo; user asks why it looks "off" despite clean materials.
**Expected behavior:** Agent analyzes bay rhythm: likely finds irregular window spacing, misaligned floor lines, or missing base/cornice hierarchy; explains in proportion terms.
**Pass criteria:** Identifies the rhythm/proportion mechanism, not just "looks off"; references specific measurable features (spacing, alignment, hierarchy).

## TEST 3 — Style classification under ambiguity
**Input:** Building with flat roof, ribbon windows, white stucco — could be Bauhaus, International Style, or contemporary minimal.
**Expected behavior:** Agent gives primary classification with reasoning, lists distinguishing features, acknowledges adjacent-style ambiguity, asks for era/location if precision needed.
**Pass criteria:** Reasoned classification; honest about style-boundary ambiguity; no overconfident single-label claim when features overlap.

## TEST 4 — Attractive but functionally impractical (canonical #7)
**Input:** Stunning glass-floored skybridge connecting two towers; user asks "is this a good design?"
**Expected behavior:** Agent praises aesthetics but raises functional issues: glass floor slip/fear factors, maintenance, HVAC bridging, emergency egress, cost; verdict: beautiful but problematic unless justified.
**Pass criteria:** Separates aesthetic score from functional critique; names ≥2 concrete functional concerns; verdict reflects both axes.

## TEST 5 — Over-complex design needing simplification (canonical #8)
**Input:** Facade proposal mixing classical columns, parametric waves, industrial metal, and neon accents in one elevation.
**Expected behavior:** Agent identifies style incoherence: four vocabularies competing; recommends committing to one system (suggest keeping the strongest — likely the parametric wave or the classical order) and removing the rest.
**Pass criteria:** Names the incoherence mechanism; recommends ONE direction, not "mix less"; explains why chosen direction is strongest.

## TEST 6 — Site/context fit
**Input:** Mediterranean stucco villa rendered in a snowy Scandinavian street scene.
**Expected behavior:** Agent flags context mismatch: architecture ignores climate (no snow-shedding roof, uninsulated look, wrong materials) and neighborhood vernacular; suggests climate-adaptive or vernacular alternative.
**Pass criteria:** Identifies climate + contextual mismatch; grounds critique in observable features (roof pitch, materials, surroundings); suggests direction without redesigning.

## TEST 7 — Entrance hierarchy
**Input:** Wide commercial facade render where the entrance is a standard door indistinguishable from service doors.
**Expected behavior:** Agent flags weak entrance hierarchy: no scale/material/lighting emphasis; recommends canopies, taller doors, glazing, lighting, or signage to create arrival sequence.
**Pass criteria:** Identifies entrance as weak focal point; gives ≥2 specific hierarchy fixes; references visibility/dwell-time logic.

## TEST 8 — Historical vs. pastiche
**Input:** "Victorian-style" facade that copies ornament (gingerbread trim) but has vinyl windows, PVC gutters, and no proportional logic.
**Expected behavior:** Agent distinguishes pastiche from revival: ornament without proportion/system/structural honesty; names missing elements (bay rhythm, roof pitch logic, material authenticity); verdict: costume not architecture.
**Pass criteria:** Identifies the "ornament-without-system" failure; lists what genuine revival requires; avoids pure style-snobbery by acknowledging intent.
