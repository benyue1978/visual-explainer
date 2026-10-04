---
name: infographic-maker
description: Use when creating or revising an educational infographic from an approved topic or content brief, including its visual brief, prompt, finished artwork, shared brand signature, review, and publishing copy. Trigger for requests to draw, generate, lay out, polish, or prepare an infographic for publication.
---

# Infographic Maker

Turn one reviewed explanation into a clear, accurate, publication-ready infographic. Keep the content model in control of the visual choices: one image should answer one learner question, and layout should reveal the mechanism rather than dictate it.

## Read project guidance first

In this repository, read:

1. The topic's `content-brief.md` and [`docs/INFOGRAPHIC_GUIDE.md`](../../docs/INFOGRAPHIC_GUIDE.md).
2. [`docs/EXPLANATION_GUIDE.md`](../../docs/EXPLANATION_GUIDE.md), [`docs/STYLE.md`](../../docs/STYLE.md), and [`docs/IMAGE_PROMPT_GUIDE.md`](../../docs/IMAGE_PROMPT_GUIDE.md).
3. [`docs/WORKFLOW.md`](../../docs/WORKFLOW.md) for source and output placement.
4. A prior visual brief and publishing-copy file when available, especially [`projects/data-representation/bits-and-bytes/visual-brief.md`](../../projects/data-representation/bits-and-bytes/visual-brief.md) and [`projects/data-representation/bits-and-bytes/publishing-copy.md`](../../projects/data-representation/bits-and-bytes/publishing-copy.md), as examples of project decisions rather than content to copy.
5. The exact shared signature [`assets/brand/learn-cs-with-us-lockup.svg`](../../assets/brand/learn-cs-with-us-lockup.svg).

If there is no reviewed content brief, draft one before generating artwork. Run a separate automated content review, resolve findings, and mark it `READY` first. User approval is optional unless requested or needed to resolve a scope decision. Outside this repository, find equivalent style, brand, and content guidance; do not invent a brand asset or claim repository-specific rules apply.

## Production sequence

1. Confirm the single learner question, audience, learning objective, main claim, scope, worked example, misconceptions, and sourced facts in the content brief. Review both factual accuracy and whether the chosen topic is sufficiently explained from useful angles. If no brief exists, draft it; then conduct a separate AI review pass (use another agent when available, otherwise a fresh reviewer role), record findings in the brief, revise, and re-review until `READY` or record unresolved blockers. If the user is working in stages, pause at their requested content checkpoint.
2. Write `visual-brief.md` with a scan path, dominant explanatory mechanism, selected supporting views and why they help, exact copy, boundaries, canvas choice, and footer safe area. Use [`docs/VISUAL_BRIEF_TEMPLATE.md`](../../docs/VISUAL_BRIEF_TEMPLATE.md). Make the title identify the actual subject or concept by name; add a question or action phrase if useful (for example, “Stacks: How Push and Pop Work?” instead of a title that names only the operations).
3. Review the visual brief separately against the `READY` content brief. Check that useful depth was carried into the composition plan; that each selected support has a learning purpose; and that an analogy is not excluded only because it repeats the mechanism. Record `READY`, `REVISE`, or `BLOCKED` and evidence in the visual brief. Revise and re-review before moving on. If the user is working in stages, pause at their requested visual-brief checkpoint; otherwise continue automatically after it is `READY`.
4. Create `image-prompt.md`: paste the style anchor from `docs/STYLE.md` unchanged, provide the verified topic mechanism and worked example, specify exact learner-facing copy, and list prohibited additions. Follow `docs/IMAGE_PROMPT_GUIDE.md`.
5. Generate or assemble the composition using the available image or design tools. Prompt for an open lower-left footer area. Never ask an image model to redraw or typeset the brand lockup. If image-generation or image-compositing tools are unavailable, prepare the editable prompt/layout/source and state which visual-production step remains.
6. Composite the exact shared SVG lockup into the lower-left reserved footer at a consistent relative size and inset. Do not alter the wording, colors, line break, or proportions. For a non-Data-Representation series, use its approved signature if the project defines one.
7. Review the final rendered image, including its brand overlay, in a separate pass against both `content-brief.md` and `visual-brief.md`, plus the style guide. Use another reviewer agent when available; otherwise switch to a fresh reviewer role. Check facts, examples, relationships, title, exact labels, composition, information depth, legibility at the expected size, palette/type/linework, and brand placement. Compare each selected element in the visual brief against the actual image: if an analogy or supporting view is missing or only mentioned in copy, it is an image issue to fix. Record evidence and corrections in `review-notes.md`, revise, and re-review until `READY` or explicitly report unresolved blockers. Put exact text, equations, or repeated geometry in editable layers when raster generation cannot keep them reliable.
8. Save the final artwork and its source artifacts alongside the topic in the existing `projects/<topic>/<piece>/` structure. Use a descriptive, lowercase kebab-case English filename, such as `eight-bits-256-patterns-infographic.png`, rather than `draft.png`.
9. Write publication metadata separately from the artwork. For Pinterest include an English title, concise description, and English tags; for the website include English alt text. Use `publishing-copy.md` and keep promotional copy off the image.
10. Report the final file path and show the image when the interface supports it. Note unresolved QA issues instead of calling the image ready to publish.

## Content and brand rules

- Preserve the approved brief's facts, central claim, scope, and distinctions. Treat its content as the factual foundation, not automatically as an exhaustive list of every useful visual or explanatory element. Do not narrow it with extra exclusions that the user did not request. A brief's boundary on new concepts or claims does not automatically prohibit a familiar teaching analogy that explains the same mechanism; only exclude analogies when the user explicitly rules them out or a specific analogy risks changing the meaning.
- Before finalizing the visual brief, consider two or three candidate supporting views that deepen the same explanation: a grounded analogy, a second state, a comparison, a misconception, a small application, or a mechanism inset. Keep each addition centered on the topic and include it because it helps the learner understand, connect, distinguish, or remember the core idea—not to increase word count. Assess complementary value as well as factual novelty: a concrete analogy can offer a second mental model or aid transfer even when the main diagram already shows the mechanism. Do not reject it solely because it reinforces the same rule. Omit candidates that add clutter or a second lesson. A metaphor is optional, never a quota.
- A teaching analogy may be added when it preserves the mechanism and does not introduce a new technical claim. Label it as an analogy, make the mapping clear, and state its useful limit when a learner could mistake it for literal implementation. Keep the sourced mechanism authoritative. For example, a stack may be compared with a pile of books: placing one on top and taking the top one off models push and pop. The analogy explains the same topic; it does not add a second data-structure lesson. If a boundary in the user-approved brief is ambiguous, propose the support in the visual brief instead of silently excluding it.
- Review for explanatory richness as well as accuracy and legibility. For every candidate detail, ask: does it clarify the same topic, and will it help this audience understand better? A sparse visual can be right for a simple idea, but do not mistake the absence of unsupported facts for a reason to remove helpful definitions, visual context, a relevant analogy, or another useful perspective.
- Build a rich explanation from on-topic perspectives; remove unrelated decoration or side lessons, but do not remove useful explanatory depth in the name of brevity.
- For this project, one byte is 8 bits. Do not insert historical discussion of that definition.
- No syllabus names/codes, examination years, chapter numbers, badges, or coverage labels on artwork. Curriculum may inform internal planning only unless the user explicitly requests a visible exam aid.
- Learner-facing artwork and Pinterest/site copy for this series are in English; internal project notes may be Chinese.
- One dominant visual should explain the central claim; selected supporting details should clarify the same question. Avoid generic equal-card grids, tiny text, and decoration without explanatory purpose.
- Keep the shared visual style recognizable, but let the topic determine the diagram and composition.
- Make the result creatively specific to the topic, rich in useful information, and easy to understand at the intended viewing size. Keep the series palette, typography roles, linework, and signature consistent; do not force topics into an identical layout or reuse a metaphor that does not fit.

## Release checklist

Use [`references/release-checklist.md`](references/release-checklist.md) before describing a draft as final. Keep review evidence and remaining caveats concise and concrete.
