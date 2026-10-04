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
Learner-facing copy + visual brief
  ↓
Fixed style anchor + topic-specific image prompt
  ↓
Image generation and composition
  ↓
Content and visual review + corrections
  ↓
Final image + source notes
```

### 1. Define the topic

Name the audience, the question to answer, and the expected level of prior knowledge. Select a scope that one infographic can explain.

### 2. Research and model the content

Use [CONTENT_GUIDE.md](CONTENT_GUIDE.md) and save `content-brief.md` in the production topic folder `projects/<topic>/`. The existing guide examples are under `projects/experiments/<topic>/`; see [experiments-brief.md](../projects/experiments/experiments-brief.md). Record source links beside important claims. Work through one concrete example and distinguish the general idea from teaching simplifications or implementation-specific details.

### 3. Plan the visual explanation

Save `visual-brief.md` with a one-sentence claim, reading path, hero mechanism, supporting details, exact labels, and image-generation constraints. Start with the mechanism and choose visual forms that make its state changes or relationships visible.

### 4. Generate a composition

Use the approved visual style block in [STYLE.md](STYLE.md) and the prompt frame in [IMAGE_PROMPT_GUIDE.md](IMAGE_PROMPT_GUIDE.md). Keep the style section fixed while the topic section changes. Use one approved Visual CS image as a style reference when useful; derive each new composition from its topic brief.

### 5. Review, edit, and export

Compare the result with its sourced content brief and style guide. Check technical relationships, exact labels, reading order, richness, legibility, and visual family resemblance. Edit only the issues that need correction. Use an editable SVG, HTML, React, or design-tool layer when the model output cannot reliably preserve exact text or structure.

### 6. Keep a topic record

Save research, prompt, visual brief, final image, and review notes in the topic folder. Record the tools used, corrections made, and any intentional project-specific choices.

## From infographic to video

When a topic needs video, reuse its sourced content, concept model, terminology, visual reference, and useful source assets. Adjust the explanation for time and narration rather than simply reading every label. Follow [VIDEO_GUIDE.md](VIDEO_GUIDE.md) for STE rewrite, scenes, animatic, narration, alignment, captions, rendering, and multimodal QA.

## Shared tools and boundaries

- **ChatGPT:** research support, concept models, scripts, visual briefs, and critique. Important claims remain linked to sources and subject to human review.
- **Image generation:** illustration and complete image drafts. It may produce inaccurate labels or visual relationships, so every output is checked.
- **Codex:** keep Markdown source files consistent; make precise SVG/HTML edits when needed; generate or revise project-specific code for a real deliverable.
- **Figma / Illustrator / InDesign / Canva / Keynote:** optional layout and typography tools when a poster needs precise manual art direction.
- **Remotion / React / SVG / Three.js / Manim / FFmpeg:** add inside a video project only when the chosen visual treatment or render process needs them.

The shared Markdown system is the reusable core. Add project code when a deliverable needs editable geometry, automation, or animation. Extract shared code after a pattern has proved useful across projects.
