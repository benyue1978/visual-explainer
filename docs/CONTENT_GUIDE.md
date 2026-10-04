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
7. **Supporting details** — useful distinctions, boundary cases, trade-offs, comparisons, or applications. Choose only the details that deepen the main explanation.
8. **Common misconceptions** — correct likely misunderstandings.
9. **Simplifications and implementation differences** — identify what is a teaching model and what varies in real systems.
10. **Sources** — direct links beside the claims they support; prioritize standards, official documentation, textbooks, and primary research.

## Richness without padding

Simple topics can still make compelling visuals through state snapshots, an example trace, a boundary case, a comparison, or a small real-world application. Complex topics need a tighter scope and a strong visual hierarchy. Do not add unrelated facts just to fill space; do not assume that more copy automatically makes a better infographic.

For the initial content draft, consider these possible visual ingredients and select the ones that help this topic:

- one main mechanism diagram;
- three to six numbered steps or state changes;
- one worked example with exact inputs and outputs;
- one contrast such as hit/miss, before/after, or inner/left join;
- one boundary case or common misconception;
- one small advanced note for a second audience level;
- a compact summary or “remember this” statement.

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
4. Three to six supporting details that deepen the main idea.
5. Two likely misconceptions and corrections.
6. Important limits, simplifications, and implementation differences.
7. A short glossary of terms that should appear in the learner-facing copy.
8. A source list with direct links.

Keep the explanation complete enough to support a rich visual composition, but
exclude details that do not help answer the central question. Do not write image
prompts, choose a visual style, or invent layout ideas yet.
```

## Content review checklist

- Can every important technical claim be traced to a source or a transparent derivation?
- Does the example obey the stated rules all the way through?
- Are addresses, values, inputs, outputs, and intermediate states clearly distinguished?
- Are examples explicitly illustrative when they are not universal?
- Are implementation-dependent choices labeled as such?
- Does the detail support the central question, or should it become a separate topic?
- Can a learner summarize the mechanism in their own words after following the steps?
