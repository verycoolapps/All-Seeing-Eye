# Aesthetic Test Cases

## TEST 1 — Beautiful render with unrealistic lighting (canonical #1)
**Input:** Photorealistic kitchen render, striking composition and materials, but every surface is lit by an impossible uniform ambient glow with no visible source and no shadow variation.
**Expected behavior:** Agent separates axes: praises composition/materials on aesthetic axis, flags lighting as physically implausible on technical axis, gives split verdict rather than one blended score.
**Pass criteria:** Explicitly distinguishes "beautiful" from "correct"; names the lighting flaw (no motivated source, no shadow gradient); verdict acknowledges both strengths and the flaw.

## TEST 2 — Luxury interior overloaded with decor (canonical #2)
**Input:** High-end living room render with marble, gold accents, velvet sofas — plus 40+ decorative objects, multiple patterns, and three competing focal points.
**Expected behavior:** Agent identifies luxury materials as strengths but flags density: competing focal points, no visual rest, pattern clash; recommends specific removals (e.g., "remove table clutter, keep one art piece") rather than "less is more."
**Pass criteria:** Names the overload mechanism (competing hierarchy, no negative space); gives 2-3 concrete subtraction suggestions; acknowledges what works.

## TEST 3 — Facade proportion comparison (canonical #3)
**Input:** Two facade proposals: A has rigorous 3m module, aligned openings, clear base/shaft/crown; B has same materials but irregular window spacing and a flat undifferentiated wall.
**Expected behavior:** Agent picks A with explicit reasoning on proportion system and facade articulation, scores both on named criteria before verdict.
**Pass criteria:** Decisive pick; criteria-based justification (proportion, rhythm, hierarchy); no hedging when one is clearly stronger.

## TEST 4 — Plastic-looking wood material
**Input:** Rendered oak floor/table that reads as smooth brown plastic: uniform color, no grain variation, mirror-ish roughness, no pores or wear.
**Expected behavior:** Agent names the material-fake tells (uniform albedo, missing grain/roughness maps, no micro-imperfections) and prescribes fixes (grain texture, roughness variation, edge wear).
**Pass criteria:** Identifies it as simulated-not-real wood; lists ≥2 specific tells; suggests concrete material fixes.

## TEST 5 — Taste judgment under stated preference
**Input:** User shows two chairs — ornate Baroque vs. minimalist Scandinavian — and says "I want warm and cozy."
**Expected behavior:** Agent picks the option matching stated preference (likely Scandinavian with warm wood/textiles, or Baroque if it reads warmer), explains in terms of the user's stated axis, not personal canon.
**Pass criteria:** Decision tied to user's stated criterion; reasoning references warmth/material/texture cues; no imposition of generic "best design" verdict.

## TEST 6 — Maximalist vs. minimalist brief
**Input:** Brief asks for "bold, maximalist gallery wall"; agent's draft is restrained and minimal.
**Expected behavior:** Agent recognizes the brief violation, regenerates or flags the mismatch between stated intent (maximalism) and output (restraint). Taste follows brief, not default.
**Pass criteria:** Explicitly connects output to brief; acknowledges maximalism can be executed well (layered but curated); does not default to minimal as "safe."

## TEST 7 — "Is this good?" open question
**Input:** User posts a mediocre product photo asking "is this good?"
**Expected behavior:** Agent gives honest split verdict: technically competent but unremarkable; names the one highest-leverage improvement; does not inflate to be polite.
**Pass criteria:** Honest verdict without false praise; specific top improvement; calibrated confidence.

## TEST 8 — Trend-vs-timeless judgment
**Input:** Two logo directions: one chasing current gradient-mesh trend, one restrained classical mark. User asks which will "age better."
**Expected behavior:** Agent reasons about trend lifecycle, picks the restrained option for longevity, but notes trend option may perform better short-term; presents trade-off.
**Pass criteria:** Distinguishes short-term vs. long-term performance; decisive pick with reasoning; acknowledges trade-off honestly.
