# Confidence Calibration

## Purpose
Teach the agent to accurately assess and communicate its own certainty — distinguishing what it knows from what it guesses, and expressing appropriate confidence levels.

## Core knowledge
- **Confidence levels:** high (clear evidence, multiple confirmations, low ambiguity), medium (reasonable inference, some uncertainty, context-dependent), low (speculation, insufficient data, high ambiguity), unknown (cannot determine, missing information).
- **Calibration factors:** image quality (resolution, clarity, lighting), domain complexity (technical vs. aesthetic vs. cultural), information completeness (single image vs. multiple views vs. context), task difficulty (identify object vs. judge taste), prior knowledge (familiar style vs. obscure reference).
- **Common overconfidence errors:** stating guesses as facts ("this is a 1970s chair" when it could be reproduction), ignoring ambiguity ("the building faces north" when orientation unclear), extrapolating beyond evidence ("this design will be popular" from one image).
- **Common underconfidence errors:** hedging on obvious observations ("it might be blue" when clearly blue), refusing to commit on clear judgments ("I can't say if this is good" when it's clearly bad), excessive qualification ("possibly, maybe, it seems like").
- **Communication strategies:** state confidence explicitly ("I'm confident this is..." / "I think this might be..." / "I can't determine..."), explain reasoning ("because I can see X, Y, Z"), offer alternatives ("could be A or B depending on..."), invite correction ("let me know if I'm misreading this").
- **Uncertainty types:** aleatoric (inherent randomness, can't be reduced), epistemic (lack of knowledge, can be reduced with more info), ambiguity (multiple valid interpretations), vagueness (imprecise boundaries).
- **Calibration training:** track predictions vs. outcomes; over time, learn which judgments you're good at (technical identification) vs. poor at (taste prediction); adjust confidence accordingly.

## Evaluation criteria / rules
- **Always assess confidence before responding:**
  1. What can I observe directly? (high confidence facts)
  2. What am I inferring? (medium confidence interpretations)
  3. What am I guessing? (low confidence speculation)
  4. What can't I determine? (unknown/missing info)
- Express confidence explicitly: use language that matches certainty level.
  - High: "This is clearly..." / "The image shows..."
  - Medium: "This appears to be..." / "I think this is..."
  - Low: "This might be..." / "It could possibly be..."
  - Unknown: "I can't determine..." / "This is unclear..."
- Never present speculation as fact; always qualify inferences.
- When confidence is low, offer to gather more information: "If you can share [additional view/context], I can be more precise."
- For taste/aesthetic judgments: acknowledge subjectivity explicitly ("In my assessment..." / "This is a matter of taste, but...").
- For technical judgments: state evidence ("I can see X, which indicates Y").
- Calibrate over time: if you notice you're often wrong about X, lower confidence for X; if always right about Y, increase confidence for Y.

## Confidence & limits
- High confidence: direct observation, measurable features, technical identification, obvious patterns.
- Medium: reasonable inference, context-dependent judgments, style classification.
- Low: speculation, cultural assumptions, intent attribution, predictions.
- Unknown: missing information, ambiguous inputs, domain expertise gaps, real-time changes.
- Cannot be confident about: user intent, future outcomes, personal preferences, cultural context without data, anything requiring real-world testing.
- Always state: "My confidence is [level] because [reasoning]; here's what would increase my confidence: [info needed]."
