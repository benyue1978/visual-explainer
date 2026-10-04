# AI feature testing: build an evaluation loop

**Audience:** Software professionals building or integrating AI-enabled features.  
**Complexity:** Advanced workflow, explained as a practical loop.  
**Status:** sourced content draft.

## Learning objective

Explain how an AI feature evaluation turns representative examples and explicit criteria into repeatable evidence for improving and releasing a system.

## Main claim

An AI feature needs a representative set of cases, task-specific grading, failure analysis, and repeat runs after changes; one aggregate score alone is not enough.

## Worked example

Use a support assistant answering from a return policy:

- Policy fact: eligible physical items can be returned within 30 days; digital gift cards are not returnable.
- Test input: “I bought shoes 14 days ago. Can I return them?”
- Expected behavior: answer yes, state the 30-day condition, and ground the answer in the policy.
- Evaluation case: store the input, relevant policy excerpt, expected behavior, and grading criteria together.

This is an illustrative test case, not a universal return policy.

## Evaluation loop

1. **Define the task and criteria.** State what good behavior means for this feature and which failures matter.
2. **Build a representative test set.** Include typical, edge, and adversarial cases drawn from domain expertise and observed use where appropriate.
3. **Run the whole system.** Capture outputs and relevant traces for the version being evaluated.
4. **Grade the outputs.** Use deterministic checks where possible, rubric/model graders for structured judgments, and human review for nuanced quality or grader calibration.
5. **Inspect failures by type.** Break results down by task slice and failure mode; a score can hide important weaknesses.
6. **Improve and rerun.** Change prompt, model, retrieval, or code; rerun the same evaluation set to check for regressions and add useful new cases over time.

## Supporting details

- The test set should resemble real inputs and the contexts in which the product will be used.
- A grader measures a defined criterion; a model grader is still a measurement instrument and should be checked against human judgment.
- A useful evaluation combines numerical results with inspection of actual outputs and failure cases.
- Treat evaluations as ongoing work: new usage patterns or failures can reveal missing cases.
- Keep test data, scoring criteria, and the system version traceable so a result can be interpreted later.

## Misconceptions and boundaries

- A high average score does not prove that every user group or failure category performs well.
- A model judge is not automatically an objective source of truth.
- A fixed test set can become unrepresentative as the product, users, or risks change.
- Evaluation does not replace live monitoring, human escalation, or broader risk management.

## Exact learner-facing copy

- `Test the AI feature, not just the prompt`
- `Build a repeatable evaluation loop`
- `Define task + criteria`
- `Build representative cases`
- `Run the system`
- `Grade against criteria`
- `Inspect failure slices`
- `Improve, then rerun`
- `Typical · Edge · Adversarial`
- `Deterministic checks`
- `Rubric / model grader`
- `Human review`
- `Human review calibrates the model grader.`
- `One score can hide a weak slice.`
- `Illustrative example (checkmarks and warning symbol are hypothetical, not measured results).`
- `Same cases. New version. Compare again.`
- `Evaluation complements monitoring.`
- `Worked example: return policy assistant`
- `Input (Typical)`
- `Policy (evidence)`
- `AI answer`
- `Grader criteria (task-specific)`
- `Answers the question`
- `States the 30-day condition`
- `Distinguishes physical vs. digital gift cards`
- `Grounds the answer in the policy`

## Sources

- [OpenAI API: Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices) — representative task-specific test sets, automated and human evaluation, scorer calibration, failure cases, and continuous evaluation. The source discusses platform-specific API lifecycle separately; this sample uses only the general evaluation practices.
- [NIST AI RMF Core: Measure](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/) — documenting test/evaluation methods and using quantitative, qualitative, or mixed approaches across the AI lifecycle.
- [OpenAI API: Working with evals](https://developers.openai.com/api/docs/guides/evals) — test data and explicit testing criteria as core ingredients of an evaluation.
