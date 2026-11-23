# Exterior Review

## When to use
Use when reviewing building exteriors, landscapes, streetscapes, urban scenes, or any outdoor visual environment — photos, renders, or site imagery.

## Inputs required
- One or more exterior images
- Optional: location/climate, building type, time-of-day intent, surrounding context
- Optional: purpose (residential facade, commercial signage zone, public realm, landscape design)

## Steps
1. **Read the scene's scale and context.** Is this a hero object in a landscape, urban fabric, or object against sky? The judging criteria differ completely by context.
2. **Sky and atmosphere.** Evaluate sky quality, cloud structure, haze, and time-of-day mood. Flat or blown skies weaken even good architecture; dramatic skies can rescue weak subjects — note which is happening.
3. **Building/landscape form.** Assess silhouette, massing, and facade composition as in architectural-review, but add: roofline treatment, ground-floor relationship to street, and how the object meets the horizon.
4. **Vegetation and landscape elements.** Judge planting scale (realistic vs. token), seasonal appropriateness, maintenance realism, and whether greenery supports or competes with the structure.
5. **Street furniture, vehicles, people.** These are scale anchors and life-signals. Flag their absence (sterile renders) or their problems (wrong scale, wrong era, distracting placement).
6. **Lighting and shadows.** Sun angle, shadow length and softness, artificial lighting presence. Check shadow direction consistency and whether shadows ground or float the objects.
7. **Color and material at distance.** Judge exterior palette for legibility from the viewing distance implied; note colors that will fade or clash.
8. **Score all dimensions**; Functional Quality and Contextual Appropriateness weighted for architecture; Originality weighted for landscape/design work.

## Output format
```
SCENE: <type + context>
ATMOSPHERE: <assessment>
FORM/MASSING: <assessment>
LANDSCAPE/LIFE: <assessment>
LIGHTING: <assessment>
SCORE TABLE: <10 dimensions>
ISSUES BY PRIORITY: <from priority-system>
VERDICT: <rating + one-line summary>
```

## Confidence handling
- HIGH: wide context shots, consistent lighting, identifiable location cues.
- MEDIUM: single building view without context — limit contextual claims; weather/season unclear.
- LOW: heavily retouched images, impossible lighting, or CGI-indistinguishable-from-photo — flag photorealism breaks explicitly (impossible shadows, repeated textures, anatomy errors in people).
