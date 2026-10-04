# Image-generation prompt · AI feature evaluation

Style anchor: `docs/STYLE.md` v1.0.
Style reference: `projects/experiments/stack-push-pop/assets/stack-push-pop.png` — style only; do not copy its stack subject or state-trace layout.
Topic source: `content-brief.md`.  
Composition: `visual-brief.md`.

```text
Use case: scientific-educational infographic for software professionals.
Audience: software engineers and product teams building AI-enabled features.
Learning goal: explain how an evaluation loop provides repeatable evidence about AI behavior.
Main claim: representative cases, explicit criteria, failure analysis, and reruns make AI feature quality measurable and improvable.

STYLE ANCHOR:
Create a polished editorial technical field guide in a relaxed, trustworthy,
professionally art-directed visual style. Use a warm ivory paper canvas, a quiet
low-saturation base, and the shared semantic palette: deep blue-black for type
and outlines, muted slate for structures, dusty teal for inputs and active paths,
muted copper for values and results, and soft coral for warnings or control
signals. Use precise vector-like diagrams, clean silhouettes, fine consistent
linework, restrained paper grain, and occasional fine hatching. Use an expressive
editorial serif for the main title, legible compact labels, and monospaced type
for code, addresses, and formulas. Build an asymmetric page around one dominant
annotated mechanism diagram, then add two to five topic-relevant supporting
details with a clear reading path. Make the page rich but orderly, with deliberate
whitespace. Keep colors, typography roles, line language, and surface treatment
recognizable across topics, while letting each topic have its own composition.
Do not use generic dashboard grids, equal-sized cards, decorative filler, neon,
purple gradients, fake technical labels, invented data, or tiny unreadable text.

STYLE REFERENCE:
Use Image 1 as a STYLE reference only. Carry over its palette roles, typography
hierarchy, linework, surface texture, illustration finish, and level of detail.
Do not copy its stack subject, values, labels, diagram, or page layout. Build a
new system-evaluation loop with a different composition.

TOPIC:
Show a repeatable loop: define task and criteria → build representative cases →
run the AI system → grade outputs → inspect failure slices → improve and rerun
the same cases. The case set includes Typical, Edge, and Adversarial examples.
Show three complementary graders: deterministic checks, a rubric/model grader,
and human review. Show human review calibrating the model grader. Include a
compact breakdown by task-specific criteria so an overall score cannot hide a
weak category. Do not invent metric values.

Worked example:
Policy: eligible physical items can be returned within 30 days; digital gift
cards are not returnable. Input: “I bought shoes 14 days ago. Can I return them?”
Good behavior: answer yes, state the 30-day condition, and ground it in the policy.
Show the case, evidence, AI answer, and grader criteria as one small trace.

COMPOSITION:
Portrait 4:5 page. Make the evaluation loop the dominant asymmetric diagram,
with the worked support-assistant example travelling through one part of it.
Use a test-case strip, a three-part grader illustration, a failure-slice inset,
and a baseline-versus-new-version rerun link. Use linework and annotations,
not a generic monitoring dashboard. Keep the professional audience in mind
without making the page look like software UI.

EXACT COPY:
“Test the AI feature, not just the prompt”
“Build a repeatable evaluation loop”
“Evaluation complements monitoring.”
“Define task + criteria”
“Build representative cases”
“Run the system”
“Grade against criteria”
“Inspect failure slices”
“Improve, then rerun”
“Typical · Edge · Adversarial”
“Deterministic checks”
“Rubric / model grader”
“Human review”
“Human review calibrates the model grader.”
“One score can hide a weak slice.”
“Illustrative example (checkmarks and warning symbol are hypothetical, not measured results).”
“Same cases. New version. Compare again.”
“Worked example: return policy assistant”
“Input (Typical)”
“Policy (evidence)”
“AI answer”
“Grader criteria (task-specific)”
“Answers the question”
“States the 30-day condition”
“Distinguishes physical vs. digital gift cards”
“Grounds the answer in the policy”
Render these labels exactly. Add no other text except the short worked example dialogue and policy supplied above.

ACCURACY:
The policy and the pass/fail slice display are illustrative examples, not measured
results. Label the slice display “Illustrative example”. Make clear that criteria
are task-specific, human judgment can calibrate automated graders, and evaluation
complements live monitoring. Do not present a model grader as infallible. Do not
fabricate scores, percentages, or reliability claims. No logo or watermark.
```
