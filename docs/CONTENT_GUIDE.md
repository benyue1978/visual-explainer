# Topic research and content preparation

This guide turns a topic into accurate, sufficiently rich material for an infographic or video. The goal is one clear explanation with enough meaningful detail to support a designed composition.

## Content package

Create a `content-brief.md` for each topic. Include:

1. **Audience and prior knowledge** — A-level, introductory university, or software professional.
2. **Learning objective** — one thing the reader should be able to explain or do.
3. **Scope** — what this piece covers and what it leaves for another piece.
4. **Main claim** — one sentence that states the central takeaway.
5. **Mechanism** — objects, inputs, state changes, outputs, and causal steps.
6. **Worked example** — real or clearly labeled illustrative values that can be traced through the mechanism.
7. **Supporting details** — explore useful distinctions, boundary cases, trade-offs, comparisons, analogies, or applications. Include the relevant perspectives that deepen the learner's explanation; use the richness review below to keep the coverage focused on the topic.
8. **Common misconceptions** — correct likely misunderstandings.
9. **Simplifications and implementation differences** — identify what is a teaching model and what varies in real systems.
10. **Sources** — direct links beside the claims they support; prioritize standards, official documentation, textbooks, and primary research.

Start from the reusable [content brief template](CONTENT_BRIEF_TEMPLATE.md).

## Explanatory richness and relevance

Once a topic has been chosen, explain it richly from the angles that help this audience understand it. Scope limits which concepts and claims belong to the piece; it does not limit the explanation to one diagram or one phrasing. Explore the mechanism, a complete example, an intuitive analogy, a comparison, a misconception, an application, and relevant limits or trade-offs. Choose the combination that gives the learner a fuller mental model. A simple topic may need only a few views; a complex one may need several connected views.

Include a detail when it adds understanding, intuition, distinction, transfer, or memory. Leave out details that are unrelated, misleading, or repeat existing material without adding a useful perspective. Do not reject an analogy or supporting explanation solely because the main mechanism is already shown.

For the initial content draft, consider these possible explanatory ingredients and select the ones that help this topic:

- one main mechanism diagram;
- three to six numbered steps or state changes;
- one worked example with exact inputs and outputs;
- one contrast such as hit/miss, before/after, or inner/left join;
- one boundary case or common misconception;
- one small advanced note for a second audience level, when appropriate;
- a compact summary or “remember this” statement.

Record the purpose of each selected detail. For an analogy, state what maps to the real mechanism and where the analogy stops.

## Reusable research prompt

Replace the bracketed fields. Research first and keep claims traceable. Do not generate an infographic until the content model is reviewed.

```text
Research the topic “[TOPIC]” for [AUDIENCE] learners.

Purpose: help the learner understand [LEARNING GOAL].
Scope: focus on [SCOPE].

Use current authoritative sources where the facts may vary or change. Prefer
official specifications, documentation, university texts, and primary research.
For each important claim, provide a source link and a short note about what that
source supports. Separate established facts, common implementations, teaching
abstractions, and uncertain or version-dependent details. Do not invent numbers.

Return:
1. A one-sentence main claim.
2. A step-by-step concept model: objects, input, state changes, output, and causal
   connections.
3. One worked example with values that can be followed from start to finish.
4. Supporting details from the useful explanatory angles for this topic; include enough depth to make the mental model clear, without treating this as a fixed count.
5. Two likely misconceptions and corrections.
6. Important limits, simplifications, and implementation differences.
7. A short glossary of terms that should appear in the learner-facing copy.
8. A source list with direct links.

Keep the explanation complete enough to support a rich visual composition, but
exclude details that do not help answer the central question. Do not write image
prompts, choose a visual style, or invent layout ideas yet.
```

## Content review process

After drafting `content-brief.md`, run a separate review pass before writing the visual brief. The reviewer may be another AI agent when available; otherwise use a fresh reviewer role and check each claim against the cited sources. Do not ask the user to review by default unless they requested staged review or the brief contains a decision only they can make. Fix issues and repeat the review until the brief is ready, or record unresolved blockers.

Review both accuracy and explanatory completeness. Check whether the brief has enough relevant depth for the selected topic, whether any useful analogy or perspective was omitted just because it repeats the central claim, and whether the scope boundary is excluding a helpful explanation rather than a separate lesson.

## Content review checklist

- Can every important technical claim be traced to a source or a transparent derivation?
- Does the example obey the stated rules all the way through?
- Are addresses, values, inputs, outputs, and intermediate states clearly distinguished?
- Are examples explicitly illustrative when they are not universal?
- Are implementation-dependent choices labeled as such?
- Does the detail support the central question, or should it become a separate topic?
- Can a learner summarize the mechanism in their own words after following the steps?
- Have useful explanatory angles been explored, including analogies, comparisons, applications, misconceptions, or limits where they fit?
- Does each exclusion protect focus, accuracy, or readability, rather than merely reducing the amount of content?
- Is every teaching analogy mapped to the mechanism and bounded where it could mislead?

Record review status (`READY`, `REVISE`, or `BLOCKED`), the reviewer's role, the findings, and any corrections in the content brief. Continue to visual planning only when status is `READY`.
