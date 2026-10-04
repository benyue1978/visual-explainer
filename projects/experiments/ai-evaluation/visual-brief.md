# Visual brief: evaluating an AI feature

Use the shared visual style in `docs/STYLE.md`. This is the complex, software-professional sample.

## Visual thesis

An evaluation is a repeatable loop: representative cases go through a system, graders inspect behavior against criteria, and failure analysis guides the next version.

## Composition

- Portrait 4:5 page; retain the same canvas, palette roles, typography, linework, and texture as the other samples.
- Make a large circular or serpentine evaluation loop the hero: define behavior → case set → system run → grading → failure analysis → improve and rerun.
- Show one concrete support-assistant case travelling through the loop: user question, policy evidence, AI answer, and criterion result.
- Add a clear test-set strip labeled Typical / Edge / Adversarial.
- Show three complementary grader types: deterministic checks, rubric/model grader, human review. Make calibration visible as a feedback link between human judgment and the grader.
- Add a result breakdown by failure slice, with a visual reminder that one overall score can conceal a weak category. If pass/fail states are shown, label them “Illustrative example”; they are not measured results. Do not invent scores.
- Add the exact note “Evaluation complements monitoring.”
- Keep text subordinate to the flow; no fake dashboards or fabricated metrics.

## Required checks

- The example return policy is explicitly illustrative and states 30 days for eligible physical items and no returns for digital gift cards.
- The example answer includes the time condition and is grounded in the policy excerpt.
- Distinguish model output from grader judgment and human review.
- Show the same cases being rerun after a system change.
- Never portray a model grader as perfectly objective or a single aggregate score as sufficient.
