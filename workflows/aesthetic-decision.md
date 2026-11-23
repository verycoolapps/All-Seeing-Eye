# Aesthetic Decision

## When to use
Use when the user asks "which is better?", "should I pick A or B?", "is this good design?", or any forced-choice between visual options where a decisive recommendation is required — not just analysis.

## Inputs required
- Two or more candidate images/options (or one image evaluated against an implicit standard)
- The decision context: what the choice is for (client approval, personal purchase, design direction, portfolio selection)
- Optional: user's stated priorities or constraints (budget, brand, timeline)

## Steps
1. **Frame the decision.** State the choice in one sentence: "Choose between X and Y for purpose Z under constraints C." If purpose is unstated, ask or infer from context — never decide without a purpose.
2. **Independent evaluation.** Score each option on all 10 rubric dimensions (visual-scoring.md). Do not compare yet — evaluate each on its own merits first to avoid anchoring.
3. **Weighted comparison.** Apply decision-matrix.md: weight criteria by the decision context (e.g., client-facing work weights Stylistic Consistency and Functional Quality; personal use weights Originality and Color Harmony). Produce weighted scores.
4. **Identify deal-breakers.** Check each option against hard constraints: if one fails a requirement (wrong format, over budget, off-brand), it is eliminated regardless of score.
5. **Check for false ties.** If scores are within 0.5, look for a tiebreaker: which option is more versatile? More distinctive? Easier to iterate on? Which would a professional choose?
6. **Make the call.** State the winner and the runner-up. If genuinely tied, say "tie — choose based on X" and specify what X is.
7. **Commit to a recommendation.** End with an explicit "MY RECOMMENDATION:" line naming the choice and the single strongest reason.
8. **Note reversibility.** If the decision is easily reversible, say so; if irreversible or costly, add a caution line.

## Output format
```
DECISION: <framed choice>
CANDIDATES: <A, B, ...>
SCORE TABLE: <weighted scores>
DEAL-BREAKERS: <eliminations or none>
WINNER: <choice>
MY RECOMMENDATION: <one decisive sentence>
CONFIDENCE: <HIGH/MEDIUM/LOW>
```

## Confidence handling
- HIGH: clear score separation (>1.0 point), no deal-breakers, purpose known.
- MEDIUM: close scores or partial information — state the deciding factor explicitly.
- LOW: missing context (no purpose, no constraints) or images too degraded to differentiate — recommend gathering the missing input rather than guessing.
