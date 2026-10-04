# Infographic production guide

An infographic starts from a well-formed explanation. The visual system should make that explanation easier to see, while each topic keeps the composition its mechanism needs.

## Standard workflow

1. **Prepare the topic** — follow [content preparation](CONTENT_GUIDE.md) and [explanation principles](EXPLANATION_GUIDE.md). Save sourced facts, a concept model, a worked example, and the copy that must appear.
2. **Write a visual brief** — state the main claim, the reader's scan path, the hero mechanism, the supporting details, and the exact labels. See the [stack](../projects/experiments/stack-push-pop/visual-brief.md), [SQL joins](../projects/experiments/sql-joins/visual-brief.md), [AI evaluation](../projects/experiments/ai-evaluation/visual-brief.md), or [CPU and memory](../projects/experiments/cpu-memory/visual-brief.md) brief for examples.
3. **Choose topic-specific visual forms** — use a state trace, cutaway, timeline, relationship map, comparison, data view, or another form that explains the mechanism. A topic can have several visual layers without becoming a grid of generic cards.
4. **Generate a composition** — combine the [brand style guide](STYLE.md) and [image-prompt template](IMAGE_PROMPT_GUIDE.md) with the topic's exact content. Use the same style anchor across topics; vary the hero illustration and layout to fit the concept.
5. **Review and revise** — check content, relationships, labels, visual hierarchy, legibility, richness, and brand consistency. Change one main issue at a time and record the final corrections.
6. **Make exact information editable when needed** — image generation can provide a full visual draft or topic illustration. Move exact text, equations, data, and arrows into SVG, a design tool, or React/TypeScript if they need precise correction or repeated updates.
7. **Export and record** — save the source brief, prompt, final image, and review notes beside the topic. Choose PNG, SVG, PDF, or a page to fit its actual destination.

## What a strong first visual should contain

- One dominant image or diagram that explains the central claim.
- Several meaningful supporting details, such as a worked example, alternative state, comparison, boundary case, or advanced note.
- A scan path that works before the reader examines every small label.
- Explicit distinctions for the concepts most likely to be confused.
- Enough detail to be valuable, with no filler or fabricated metrics.

## Tool roles

- **ChatGPT:** research support, concept model, learner-facing copy, visual brief, and critique.
- **Image model:** composition design, editorial illustrations, or a complete infographic draft.
- **Codex:** maintain research and prompt files, make precise SVG/HTML edits when useful, and help revise assets.
- **Figma / Illustrator / InDesign / Canva / Keynote:** optional manual layout and typography tools; use them when the source needs direct art direction or precise text control.

The repository does not require a React component library to start an infographic. Add code or shared components when a real output needs editable geometry, animation, or a pattern that has repeated across topics.

## Final review gate

Before calling an image ready to publish, verify its text and numbers against the content brief; check that arrows and relationships match the concept model; confirm that the title, hero, and takeaway read in the intended order; view it at the expected display size; and compare its color, typography roles, linework, texture, and information density with the current style guide.
