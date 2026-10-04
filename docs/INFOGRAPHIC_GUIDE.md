# Infographic production guide

An infographic starts from a well-formed explanation. The visual system should make that explanation easier to see, while each topic keeps the composition its mechanism needs.

The design goal is a creative, information-rich infographic that is easy to understand and clearly belongs to the same visual series. Keep the palette, typography roles, linework, and publisher signature consistent; let the topic determine its own visual metaphor and composition.

## Standard workflow

1. **Prepare and review the content brief** — follow [content preparation](CONTENT_GUIDE.md) and [explanation principles](EXPLANATION_GUIDE.md). Save sourced facts, a complete concept model, a worked example, and relevant supporting angles. Run an accuracy-and-richness review and record `READY`, `REVISE`, or `BLOCKED` in the brief.
2. **Write and review a visual brief** — state the learner question and claim, scan path, hero mechanism, selected supporting views and why each helps, exact labels, and boundaries. Use [`VISUAL_BRIEF_TEMPLATE.md`](VISUAL_BRIEF_TEMPLATE.md). Review the visual brief against the ready content brief before prompting or generating anything.
3. **Choose topic-specific visual forms** — use a state trace, cutaway, timeline, relationship map, analogy, comparison, data view, or another form that explains the mechanism. A topic can have several connected visual layers without becoming a grid of generic cards.
4. **Generate a composition** — combine the [brand style guide](STYLE.md) and [image-prompt guide](IMAGE_PROMPT_GUIDE.md) with the topic's exact content and approved visual brief. Use the same style anchor across topics; vary the hero illustration and layout to fit the concept.
5. **Run a separate visual and content review** — compare the image against both briefs and the style guide. Check accuracy, every selected supporting view, whether an analogy is visibly and correctly mapped, visual hierarchy, legibility, richness, and brand consistency. Record findings in `review-notes.md`, correct issues, and review again.
6. **Make exact information editable when needed** — image generation can provide a full visual draft or topic illustration. Move exact text, equations, data, arrows, and other required visual details into SVG, a design tool, or React/TypeScript if they need precise correction or repeated updates.
7. **Export and record** — composite the shared brand signature from [`assets/brand/learn-cs-with-us-lockup.svg`](../assets/brand/learn-cs-with-us-lockup.svg) into its reserved footer area. Save the content brief and its review, visual brief and its review, prompt, final image, publishing title, concise description, tags, alt text, and final review notes beside the topic. Keep publishing metadata separate from the artwork and write it in the destination language.

## What a strong first visual should contain

- One dominant image or diagram that explains the central claim.
- Several meaningful supporting details, such as a worked example, alternative state, comparison, boundary case, or advanced note.
- A scan path that works before the reader examines every small label.
- Explicit distinctions for the concepts most likely to be confused.
- Enough connected detail to give the learner a useful mental model, without unrelated side topics or fabricated metrics.

## Tool roles

- **ChatGPT:** research support, concept model, learner-facing copy, visual brief, and critique.
- **Image model:** composition design, editorial illustrations, or a complete infographic draft.
- **Codex:** maintain research and prompt files, make precise SVG/HTML edits when useful, and help revise assets.
- **Figma / Illustrator / InDesign / Canva / Keynote:** optional manual layout and typography tools; use them when the source needs direct art direction or precise text control.

The repository does not require a React component library to start an infographic. Add code or shared components when a real output needs editable geometry, animation, or a pattern that has repeated across topics.

## Final review gate

Use an independent automated review pass when available; otherwise switch to a fresh reviewer role and check the evidence explicitly. User review is optional unless requested or needed to resolve a decision. Before calling an image ready to publish:

- verify text, numbers, claims, and examples against the ready content brief;
- check that arrows, grouping, and analogy mappings match the concept model;
- compare every selected element in the visual brief against the actual image and flag omissions or weak visualizations;
- confirm the title, hero, supporting views, and takeaway form a clear reading order;
- view the image at its expected display size and check legibility, hierarchy, richness, and visual balance;
- compare color, typography roles, linework, texture, density, and brand placement with the style guide;
- record findings and corrections in `review-notes.md`, then repeat the review after edits.

Mark the image `READY` only when factual and visual blockers are resolved and the selected explanation is both accurate and sufficiently clear.
