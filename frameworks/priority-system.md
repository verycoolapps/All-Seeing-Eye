# Priority System

The pipeline for turning visual analysis into prioritized, actionable improvement recommendations.

## The Pipeline

```
OBSERVE → UNDERSTAND → DIAGNOSE → PRIORITIZE → DECIDE → RECOMMEND → VERIFY
```

### 1. OBSERVE
Capture the raw visual facts: what is literally present — objects, colors, lighting, composition, defects. No interpretation yet. List everything visible without judgment.

### 2. UNDERSTAND
Interpret what the observation means: what is the image/space trying to communicate? Who is the audience? What emotions or conclusions does it produce? What is the gap between intent and effect?

### 3. DIAGNOSE
Identify root causes of problems. Don't stop at symptoms ("the lighting is bad") — find why ("single overhead source creates harsh shadows and no depth; no fill light; color temperature too cool for the warm materials").

### 4. PRIORITIZE
Rank all diagnosed issues using Impact × Effort:

| Priority | Impact | Effort | Action |
|----------|--------|--------|--------|
| **P1 — Critical** | High | Low–Medium | Do first. Blocks function or severely damages impression. |
| **P2 — High** | High | High | Plan for; major improvement but requires investment. |
| **P3 — Medium** | Medium | Low | Quick polish; do when convenient. |
| **P4 — Low** | Low | Any | Nice-to-have; only if time/budget allows. |

Impact = how much the issue hurts the overall impression or function (1–5).
Effort = cost, time, skill, or disruption required (1–5).
Priority score = Impact × (6 − Effort). Higher = do sooner.

### 5. DECIDE
For each prioritized issue, decide the recommended change using decision-matrix.md. If multiple options exist, score them and pick the best.

### 6. RECOMMEND
Produce the improvement record for each issue:

```
EXISTING CONDITION: <what is there now>
WEAKNESS: <what is wrong with it>
ROOT CAUSE: <why it is wrong>
RECOMMENDED CHANGE: <specific, actionable fix>
EXPECTED BENEFIT: <what improves and by how much>
TRADE-OFF: <what is sacrificed or risked>
PRIORITY: <P1/P2/P3/P4>
```

### 7. VERIFY
After implementation (or in review of proposed changes), re-run OBSERVE on the result. Does the change actually fix the diagnosed problem? Did it introduce new issues? Loop back to DIAGNOSE if needed.

## Quick Reference: Impact vs. Effort Matrix

```
              LOW EFFORT          HIGH EFFORT
HIGH IMPACT   → P1: DO NOW        → P2: PLAN
LOW IMPACT    → P3: POLISH        → P4: DEFER
```
