# Compare Images

## When to use
Use when two or more images must be compared — before/after edits, design variants, competitor references, render iterations, or "which is better" decisions.

## Inputs required
- Two or more images (minimum 2)
- Comparison axis if known: same subject different versions, different subjects same criteria, or open-ended ranking
- Optional weighting: which criteria matter most for the decision

## Steps
1. **Normalize the comparison.** State what is being held constant and what varies. If images differ in subject, scale, or medium, acknowledge that some criteria are not directly comparable.
2. **Inventory each image independently.** Run a fast analyze-image pass on each: subject, composition, technical quality, message.
3. **Build the comparison table.** For each scoring dimension (visual-scoring rubric), rate every image 0–10. Mark dimensions as N/A when not applicable to one image's content type.
4. **Identify decisive differences.** Which 2–4 differences actually drive the decision? Weight them explicitly rather than averaging everything equally.
5. **Check comparability traps.** Beware: different resolutions, different crops, different lighting conditions, different color profiles, or one image being a photo vs. a render — these distort direct comparison. Note them.
6. **Apply the decision matrix** if the comparison is for a selection/approval decision: score each candidate on functional suitability, aesthetic quality, feasibility, contextual fit, requirements coverage, cost, maintenance, accessibility, sustainability, risk — weighted per priority-system.
7. **Declare a winner or a tie.** If scores are within 0.5 points, declare a tie and state what additional evidence would break it. Never manufacture a winner.
8. **Justify.** One paragraph: the top reasons the winner wins, and the top reason the loser loses.

## Output format
```
COMPARISON: <images A vs B vs C>
HELD CONSTANT: <what's equal>
VARIES: <what differs>
SCORE TABLE: <dimension | A | B | C>
DECISIVE FACTORS: <ranked list>
COMPARABILITY CAVEATS: <list or none>
RESULT: <winner / tie / conditional>
RECOMMENDATION: <MY RECOMMENDATION statement>
```

## Confidence handling
- HIGH: same subject, similar conditions, clear scoring gaps.
- MEDIUM: comparable but with caveats (different cameras, lighting, or compression).
- LOW: images are fundamentally different in type or quality — treat as independent analyses and compare only on shared dimensions. State that a direct verdict is unreliable.
