# Architectural Intelligence

## Purpose
Enable expert-level reading and judgment of buildings — facades, massing, structure, proportion systems, and architectural style — for critique, selection, and generation tasks.

## Core knowledge
- **Massing vocabulary:** extrude, carve, cantilever, terrace, tower, plinth, cornice, setback, hip/gable/flat roof, curtain wall, punched openings vs. ribbon windows.
- **Proportion systems:** classical orders (Tuscan→Corinthian), module/grid logic, golden-section facades, human-scale bays (~3-4m), floor-to-floor heights (3-4m residential/commercial).
- **Structural honesty:** columns should land on structure; cantilevers need plausible depth; curtain walls need mullion rhythm; arches need abutment mass. Floating or unsupported elements read as fake.
- **Facade rhythm:** window spacing, floor alignment, entrance emphasis, base/shaft/capital hierarchy of tall buildings, horizontal vs. vertical emphasis.
- **Style signatures:** Art Deco (stepped geometry, sunburst), Bauhaus (flat roofs, ribbon windows, white volumes), Brutalism (béton brut, massive forms), Gothic (pointed arches, verticality), Parametric (fluid forms), Vernacular (local materials, pitched roofs).
- **Environmental logic:** orientation (south glazing for passive solar), shading devices, entrance orientation for weather, roof pitch for drainage/snow.
- **Scale cues:** door height, stair slope, window-to-wall ratio, human silhouettes in renders.

## Evaluation criteria / rules
- Evaluate architecture on: structural plausibility → proportion/system → facade articulation → style coherence → environmental logic → craft detail.
- When generating facades, commit to ONE proportion system and ONE style logic; mixed vocabularies read as noise.
- Flag "render tells": perfectly clean concrete, unrealistically large glazing, missing AO/contact shadows, impossible cantilever lengths, duplicated windows at wrong spacing.
- For comparisons (facade A vs B), score each axis explicitly before the verdict.
- Check circulation implication: entrances must be reachable, stairs plausible, floor plates not absurdly deep.

## Confidence & limits
- High confidence: structural impossibilities, proportion violations, style misclassification between clear styles.
- Medium: style nuances (late vs. early period), "timeless" quality, regional appropriateness.
- Cannot assert: building codes compliance, engineering feasibility of complex geometry, historical accuracy without reference, cost.
- If unsure of style, say so and describe observed features rather than guessing a label.
