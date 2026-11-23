# Spatial Intelligence

## Purpose
Enable precise reasoning about 3D space from images and descriptions — depth relationships, scale, occlusion, viewpoint, and the ability to infer what is hidden or what would change from a different angle.

## Core knowledge
- **Viewpoint analysis:** identify camera height (eye-level ~1.6m, low angle = power, high angle = overview), lens character (wide = distortion/stretching, telephoto = compression/flattening), and how these distort perception.
- **Depth ordering:** near/mid/far layers; occlusion boundaries; atmospheric perspective (distant = lighter, less saturated, lower contrast); defocus gradient.
- **Scale estimation:** anchor objects (human ~1.7m, door ~2.1m, car ~4.5m, stair riser ~18cm); room sizes (bedroom 3x4m minimum, living room 4x5m comfortable); furniture footprints.
- **Spatial relationships:** adjacency ("next to," "across from"), containment ("inside," "between"), direction ("left of," "behind," "above") — must be consistent in all descriptions.
- **Hidden-space inference:** what the camera cannot see (behind camera, through walls, under furniture); state explicitly what is unknown.
- **Plan vs. elevation reading:** a facade photo shows one elevation; the building has four sides + roof. Infer but flag assumptions.
- **Proportion in image:** foreshortening, vanishing points, horizon line position (rule of thirds often places it there).
- **Multi-view synthesis:** when given several images of one space, reconcile them into one mental model; flag contradictions.

## Evaluation criteria / rules
- Always establish the viewpoint before describing contents: "Eye-level shot from doorway looking north..."
- Use consistent spatial language; never say "on the left" without anchoring to the viewer or a landmark.
- When asked "what's behind X?" answer with probability or "cannot determine from this image."
- For redesign/edit tasks, specify changes in spatial terms ("move the sofa 0.5m toward the window") not vague directions.
- Detect impossible geometry: objects intersecting, impossible overlaps, scale violations (a coffee table wider than the sofa).
- Flag when a single image is insufficient for the requested task and request additional views.

## Confidence & limits
- High confidence: visible spatial relationships, occlusion, depth order, obvious scale anchors.
- Medium: hidden-space inference, exact distances (only from known references), plan reconstruction from one photo.
- Cannot assert: exact measurements without reference objects, what's outside the frame, structural internals, true 3D geometry from a single 2D image.
- Always caveat: "From this angle..." or "Appears to be..." when depth is ambiguous.
