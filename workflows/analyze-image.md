# Analyze Image

## When to use
Use this workflow when given a single image — a photograph, render, screenshot, or scan — that needs structured visual analysis: what it is, what it communicates, and how well it works.

## Inputs required
- One image (URL, local path, or embedded attachment)
- Optional context: what the image is supposed to accomplish (e.g., "render for a restaurant menu," "facade photo for a residential project")
- Optional constraints: target audience, medium (print vs. digital), scale of subject

## Steps
1. **Frame the assignment.** Restate in one line what the image is and what evaluation target applies (portfolio piece, marketing asset, document scan, art critique).
2. **First-pass inventory.** List every visible element: subjects, objects, people, text, UI elements, watermarks. Note exact colors only where they carry meaning (brand colors, alert colors).
3. **Composition read.** Identify the dominant subject, focal path, balance of mass, negative space usage, and whether the eye is guided or confused. Note cropping and viewpoint (eye-level, low angle, top-down).
4. **Technical assessment.** Judge exposure, focus/sharpness, noise, compression artifacts, color accuracy, resolution adequacy for intended use. Flag issues as critical vs. cosmetic.
5. **Content & context read.** What does the image claim? What mood, status, or message does it project? Does it match the stated intent?
6. **Aesthetic evaluation.** Apply the visual-scoring rubric: rate Composition, Proportion, Color Harmony, Material Quality, Lighting, Visual Hierarchy, Stylistic Consistency, Originality, Functional Quality, Overall Excellence (0–10 each).
7. **Defect list.** Enumerate concrete problems ordered by severity: blocking errors first (blurry subject, clipped highlights, wrong crop), then quality issues, then polish opportunities.
8. **Verdict.** State whether the image succeeds at its job, partially succeeds, or fails — with one sentence of justification.

## Output format
```
ANALYSIS: <one-line identity>
CONTEXT MATCH: <aligned / partially / misaligned>
SCORES: see rubric table
STRENGTHS: <bullets>
DEFECTS: <severity-ordered bullets>
VERDICT: <PASS / CONDITIONAL / FAIL>
CONFIDENCE: <HIGH / MEDIUM / LOW + reason>
```

## Confidence handling
- HIGH: clear subject, good resolution, single obvious interpretation.
- MEDIUM: heavy compression, ambiguous subject, or intent unclear — state assumptions.
- LOW: image is damaged, extremely low-res, or context-dependent (e.g., requires knowing proprietary brand guidelines). Say what additional input would raise confidence.
