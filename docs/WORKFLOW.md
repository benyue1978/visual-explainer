# End-to-end production workflow

Use Markdown as the shared source of truth for brand style, content, prompts, and production decisions. Each topic carries the research and outputs it needs. Follow the infographic path for static work and the video process when a topic needs animation.

## Topic to infographic

```text
Topic and audience
  ↓
Research + sources
  ↓
Concept model + worked example
  ↓
Content brief → accuracy and richness review → READY
  ↓
Visual brief → coverage and design review → READY
  ↓
Fixed style anchor + topic-specific image prompt
  ↓
Image generation and composition
  ↓
Final image review against both briefs and style → corrections → READY
  ↓
Final image + review records
```

### 1. Define the topic

Name the audience, the question to answer, and the expected level of prior knowledge. Select a scope that one infographic can explain.

### 2. Research and model the content

Use [CONTENT_GUIDE.md](CONTENT_GUIDE.md) and [CONTENT_BRIEF_TEMPLATE.md](CONTENT_BRIEF_TEMPLATE.md), then save `content-brief.md` in the production topic folder `projects/<topic>/`. Record source links beside important claims. Work through one concrete example and distinguish the general idea from teaching simplifications or implementation-specific details. Then perform and record a separate accuracy-and-richness review; do not move to visual planning until it is ready.

### 3. Plan the visual explanation

Save `visual-brief.md` with a one-sentence claim, reading path, hero mechanism, selected supporting details and their learning purpose, exact labels, and image-generation constraints. Use [VISUAL_BRIEF_TEMPLATE.md](VISUAL_BRIEF_TEMPLATE.md). Review it against the ready content brief: confirm that the visual plan preserves the explanation's useful depth and that each selected analogy or perspective has a clear job. Record `READY`, `REVISE`, or `BLOCKED` before generation.

### 4. Generate a composition

Use the approved visual style block in [STYLE.md](STYLE.md) and the prompt frame in [IMAGE_PROMPT_GUIDE.md](IMAGE_PROMPT_GUIDE.md). Keep the style section fixed while the topic section changes. Use one approved Visual CS image as a style reference when useful; derive each new composition from its topic brief.

### 5. Review, edit, and export

Run a separate review of the rendered result against both the content brief and visual brief, as well as the style guide. Verify the facts, relationships, exact labels, selected supporting views, visual mapping of any analogy, reading order, richness, legibility, and visual family resemblance. Record findings in `review-notes.md`, correct issues, and repeat the review. Use an editable SVG, HTML, React, or design-tool layer when the model output cannot reliably preserve exact text or structure. Mark `READY` only after factual and visual blockers are resolved.

### 6. Keep a topic record

Save research, prompt, content and visual briefs with their review records, final image, publishing copy, and final review notes in the topic folder. Record the tools used, corrections made, and any intentional project-specific choices.

## From infographic to video

When a topic needs video, reuse its sourced content, concept model, terminology, visual reference, and useful source assets. Adjust the explanation for time and narration rather than simply reading every label. Follow [VIDEO_GUIDE.md](VIDEO_GUIDE.md) for STE rewrite, scenes, animatic, narration, alignment, captions, rendering, and multimodal QA.

## Shared tools and boundaries

- **ChatGPT:** research support, concept models, scripts, visual briefs, and critique. Important claims remain linked to sources and subject to human review.
- **Image generation:** illustration and complete image drafts. It may produce inaccurate labels or visual relationships, so every output is checked.
- **Codex:** keep Markdown source files consistent; make precise SVG/HTML edits when needed; generate or revise project-specific code for a real deliverable.
- **Figma / Illustrator / InDesign / Canva / Keynote:** optional layout and typography tools when a poster needs precise manual art direction.
- **Remotion / React / SVG / Three.js / Manim / FFmpeg:** add inside a video project only when the chosen visual treatment or render process needs them.

The shared Markdown system is the reusable core. Add project code when a deliverable needs editable geometry, automation, or animation. Extract shared code after a pattern has proved useful across projects.
