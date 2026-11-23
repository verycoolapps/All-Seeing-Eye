# Humanoid Visual Analysis

## Purpose
Analyze human figures in images and 3D models — anatomy, proportion, pose, expression, clothing, and the uncanny valley — for character design, avatar QA, and figure critique.

## Core knowledge
- **Proportion canon:** adult ~7.5-8 heads tall; head = chin to crown; shoulder width ~2 head-widths; hip width ~1.5 head-widths; hand length ~face length (chin to hairline); foot ~head length; elbow at waist, wrist at mid-thigh; knee at mid-calf.
- **Skeletal landmarks:** 7 cervical, 12 thoracic, 5 lumbar vertebrae; scapula, clavicle, pelvis as primary mass drivers; joints (shoulder, elbow, wrist, hip, knee, ankle) as pivot points for pose.
- **Muscle groups:** deltoids, pectorals, latissimus, biceps/triceps, forearm flexors, abdominals, quadriceps/hamstrings, calves, glutes; surface anatomy follows muscle bellies, not bone.
- **Pose analysis:** contrapposto (weight shift creates S-curve spine), action lines (gesture drawing principle), weight distribution (plumb line through stance foot), balance (center of mass over base of support).
- **Facial anatomy:** eye line (mid-head), nose bottom ~mid-head, mouth ~2/3 down; facial thirds (hairline-brow, brow-nose, nose-chin); expression via eyebrow angle, mouth curvature, eye openness.
- **Clothing logic:** fabric drapes follow body forms + gravity; seams at stress points; folds radiate from joints; silhouettes read gender/era/style.
- **Uncanny valley:** near-human but slightly off (eyes, skin texture, proportions) triggers discomfort; causes include asymmetric eyes, wrong gaze, plastic skin, impossible proportions.

## Evaluation criteria / rules
- For 3D humans: check head-body ratio → limb lengths → joint placement → muscle definition → pose plausibility → facial features → clothing fit.
- Flag common AI-human errors: too-perfect symmetry, fused fingers, melting joints, wrong hand count, eyes too close/far apart, hair as solid helmet, clothing clipping through body.
- For photos/art: assess anatomy accuracy (joint positions, muscle engagement), expression clarity, gaze direction intent.
- Pose must show weight and intent: a figure standing straight with arms at sides reads as mannequin, not human.
- Hands and feet are highest-detail areas; check finger count, knuckle definition, toe separation.
- Clothing must respond to pose: fabric tension at elbows/knees, drape over curves, no floating hemlines.

## Confidence & limits
- High confidence: obvious proportion breaks (>10% off canon), missing/extra fingers, impossible joint angles, facial feature misplacement.
- Medium: "awkward pose," "unnatural expression," style-appropriate anatomy (stylized vs. realistic).
- Cannot assert: exact muscle engagement without biomechanics data, emotional state from expression alone, medical/anatomical accuracy for pathological poses.
- Always specify style context: anime/chibi/stylized figures intentionally break realism canon.
