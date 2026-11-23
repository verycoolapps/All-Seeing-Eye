# Decision Matrix

Weighted evaluation framework for choosing between options or approving/rejecting a design.

## The 10 Criteria

| # | Criterion | What it measures |
|---|-----------|------------------|
| 1 | Functional Suitability | Does it do the job? Performance, usability, purpose-fit. |
| 2 | Aesthetic Quality | Visual appeal, rubric scores, craft. |
| 3 | Technical Feasibility | Can it be built/executed with available tools, skills, budget? |
| 4 | Contextual Appropriateness | Does it fit culture, climate, brand, neighbors, regulations? |
| 5 | User Requirements | Does it meet the explicit brief and implicit needs? |
| 6 | Cost | Budget impact including hidden costs (maintenance, iteration). |
| 7 | Maintenance | Long-term upkeep burden — cleaning, repair, updating, degradation. |
| 8 | Accessibility | Can all intended users access, read, and use it? |
| 9 | Sustainability | Environmental impact, material sourcing, energy use, lifespan. |
| 10 | Risk | What could go wrong? Approval, safety, reversibility, reputation. |

## Weighting
Assign weights 1–5 per criterion based on context:
- **5:** Critical — decision fails without it.
- **4:** Very important.
- **3:** Important but negotiable.
- **2:** Nice to have.
- **1:** Minor consideration.

## Scoring
For each criterion, score each option 0–10 (visual-scoring logic).
`Weighted Score = Σ (Criterion Score × Weight) / Σ Weights`

## Decision Levels

| Level | Name | Criteria | Action |
|-------|------|----------|--------|
| 1 | **Critical** | Any weight-5 criterion scores ≤ 4, or a deal-breaker exists | Reject immediately. |
| 2 | **High** | Weighted score < 6.0, or any weight-4 criterion scores ≤ 5 | Reject unless no alternatives exist; document why. |
| 3 | **Refinement** | Weighted score 6.0–7.9 | Acceptable but improvable; recommend specific fixes before approval. |
| 4 | **Optional** | Weighted score ≥ 8.0 | Strong candidate; approve or use as benchmark. |

## MY RECOMMENDATION Rule
1. Eliminate all Level 1 candidates.
2. Among remaining, pick the highest weighted score.
3. If top two are within 0.5 points, apply tiebreakers in order: (a) higher Functional Suitability, (b) lower Risk, (c) higher Originality.
4. State the decision as:

```
MY RECOMMENDATION: Choose <option> because <single strongest reason>. <Option B> is the runner-up; it loses on <criterion>.
```

Never end with "it depends" — name the dependency and give a conditional recommendation.
