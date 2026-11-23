# Quality Assurance

## Purpose
Define and enforce quality standards for visual outputs — pre-delivery checks, technical validation, aesthetic review, and the systematic prevention of common failures.

## Core knowledge
- **QA dimensions:** technical correctness (no artifacts, proper resolution, correct colors), aesthetic quality (composition, lighting, materials), functional fit (meets brief, usable in context), consistency (matches brand/style/references), accessibility (contrast, readability, inclusive design).
- **Pre-flight checklist:** before delivery, verify: resolution meets spec, colors are accurate (not oversaturated/shifted), no artifacts (aliasing, z-fighting, clipping), text is readable, links work, file format correct, naming convention followed.
- **Common failure modes:** blown highlights, crushed shadows, color banding, compression artifacts, misaligned elements, inconsistent spacing, typos, broken images, wrong aspect ratio, missing alt text.
- **Automated vs. manual checks:** automated (file size, resolution, color profile, linting) catches technical issues; manual (visual review, usability test, stakeholder approval) catches aesthetic/functional issues; both required.
- **Iterative QA:** first pass = self-review (catch obvious issues), second pass = peer review (fresh eyes), third pass = stakeholder/user testing (real-world validation); don't skip stages.
- **Severity classification:** critical (blocks delivery: broken, unreadable, wrong), major (significantly impacts quality: poor contrast, obvious artifacts), minor (polish issues: slight misalignment, suboptimal spacing), nitpick (personal preference).
- **Regression testing:** when fixing issues, verify you didn't break something else; check related elements, different screen sizes, different contexts.
- **Documentation:** log issues found, fixes applied, decisions made; helps future projects and team learning.

## Evaluation criteria / rules
- **Always run through QA checklist before declaring "done":**
  1. Technical: resolution, format, file size, no artifacts, colors accurate
  2. Aesthetic: composition, lighting, materials, typography, spacing
  3. Functional: meets brief, usable, accessible, performant
  4. Consistency: matches brand/style/references, no drift
  5. Context: works in target environment (web, print, mobile, presentation)
- Classify every issue by severity; fix critical first, then major, then minor if time permits.
- Never deliver work with known critical issues; "it's good enough" is not acceptable for broken/unreadable output.
- For subjective quality: get second opinion (peer, user, automated tool); don't rely on single judgment.
- Document QA process: what was checked, what was found, what was fixed; enables process improvement.
- For batch work: sample-check first, then full review if samples pass; don't assume consistency without verification.
- Flag when QA reveals systemic issues (e.g., "all images have color cast" = lighting setup problem, not individual image problem).

## Confidence & limits
- High confidence: technical errors (wrong resolution, artifacts, broken links), spec violations, accessibility failures.
- Medium: aesthetic quality assessments, "looks professional," usability judgments.
- Low: user preference prediction, market reception, long-term maintainability.
- Cannot QA: work requiring specialized tools (print proofs, device testing), subjective creative direction, work-in-progress by design.
- Always state: "QA based on [checklist/criteria]; real-world testing may reveal additional issues."
