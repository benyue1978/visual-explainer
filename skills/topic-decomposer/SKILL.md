---
name: topic-decomposer
description: Use when a user wants a subject, course, or syllabus turned into a concept-led learning path or a set of infographic topics. Break the subject into coherent themes, choose useful granularity, and audit concept coverage internally; use a syllabus such as Cambridge as a planning reference when requested, never as the organizing structure or learner-facing artwork unless the user explicitly asks for that.
---

# Topic Decomposer

Turn a broad subject into an understandable, teachable sequence of topics. Work from learner knowledge and conceptual dependencies. A syllabus can help identify concept families, but content and explanation drive the design.

## Start with the project context

For this repository, read these in order:

1. [`docs/EXPLANATION_GUIDE.md`](../../docs/EXPLANATION_GUIDE.md) for audience, scope, concept models, and ordering.
2. [`docs/CONTENT_GUIDE.md`](../../docs/CONTENT_GUIDE.md) and [`docs/CONTENT_BRIEF_TEMPLATE.md`](../../docs/CONTENT_BRIEF_TEMPLATE.md) for the required content model and evidence standard.
3. The target project's `README.md`, `infographic-catalogue.md`, and `coverage-matrix.md` if they exist. For Data Representation, the catalogue is an adjustable estimate, not a fixed deliverable count.
4. Any approved design spec or prior user decisions in `docs/superpowers/specs/` that govern the target series.

If this skill is used outside this repository, apply its method without assuming these paths exist. Locate equivalent project guidance; if none exists, state the assumptions briefly.

## Workflow

1. Identify the audience, what they already know, the intended learning outcome, and the requested curriculum or scope. Ask only for information that materially changes the breakdown; otherwise state reasonable assumptions and proceed.
2. Build a concept inventory from reliable source material and the project's briefs. Keep facts, prerequisite concepts, procedures, comparisons, and misconceptions distinct.
3. Organize concepts in a learning sequence based on prerequisites and cause-and-effect. Group concepts that share a natural learner question and explanatory mechanism.
4. Decide granularity using the criteria below. Give a working estimate, not a promise of final artwork count.
5. If a syllabus was requested, make an internal concept-family coverage audit: identify represented, missing, overlapping, or out-of-scope families. Do not let exact objective numbering or year-by-year versions dictate the learner's sequence unless the user explicitly requests that audit.
6. Produce the topic map and explain boundary decisions. Mark uncertain examples as seeds that still need research, not verified facts.
7. Save the result in the existing project structure when asked to update the repository. For this project, update `projects/<topic>/infographic-catalogue.md` and its README references rather than inventing a new top-level hierarchy.

When the user asks to plan first, return the proposed map and count, then pause for their review before drafting individual content briefs. If they say to proceed one at a time, prepare only the next selected topic's sourced content brief and pause for review before moving to another topic or visual design. Do not manufacture approval gates for routine tasks when the user has already delegated the full workflow.

## Granularity rules

Each proposed infographic should answer one learner question and have one central claim. Keep a topic together when its ideas share a mechanism and can be explained with one traceable worked example at readable size. Split it when it introduces a different mechanism, prerequisite, learner question, or example that cannot remain legible without crowding. Merge adjacent topics only when they share a natural explanation and the combined example clarifies both.

Do not use “one syllabus bullet = one infographic” or “one keyword = one infographic.” Estimate scope from the real explanatory work. Make clear that the count may change after individual content briefs and visual briefs are reviewed.

## Curriculum use and learner-facing boundaries

- Treat Cambridge or another curriculum as an optional planning lens when requested, not the content's purpose.
- Prefer concept families and meaningful learner questions over year-specific objective matching.
- Keep syllabus codes, exam years, chapter numbers, coverage labels, and exam badges out of learner-facing infographic plans and artwork. Only include them if the user explicitly overrides this project rule.
- Do not add historical or peripheral detail unless it helps explain the mechanism. In the Data Representation project, state directly that one byte is 8 bits; do not burden the explanation with the history of that convention.
- Preserve the project's content-first principle: no image prompt or visual layout is required at topic-mapping stage.

## Output format

Use the reusable format in [`references/topic-map-template.md`](references/topic-map-template.md). At minimum include audience and assumptions, organizing principle, ordered topic map, the learner question and boundary for each proposed piece, dependencies, an adjustable count estimate, and internal coverage findings when relevant. Keep internal curriculum notes visibly separate from learner-facing topic titles.

## Quality check

Before returning the map, verify that the sequence has no unexplained prerequisite jumps; every item has a distinct learner question; the count is labeled provisional; adjacent items have explicit boundaries; coverage notes do not leak into artwork; and no unverified example is presented as a fact. The next production step is one sourced `content-brief.md` at a time, using the project template.
