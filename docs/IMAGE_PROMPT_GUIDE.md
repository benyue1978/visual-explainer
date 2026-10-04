# Image generation prompts and workflow

Use this guide with the approved brand anchor in [STYLE.md](STYLE.md) and the topic facts in a project's `content-brief.md`. Production topics live in `projects/<topic>/`; guide examples live in `projects/experiments/<topic>/`.

## Prompt structure

Paste the style anchor unchanged into each infographic prompt. Fill in the topic and composition from that project's briefs. When using a reference image, attach one approved Visual CS output and state that it guides visual style only; derive the new subject and layout from the new topic brief.

Use this order:

1. use case and audience;
2. learning goal and one-sentence claim;
3. fixed style anchor from `STYLE.md`;
4. topic objects, causal mechanism, and worked example;
5. topic-specific composition and visual density;
6. exact learner-facing copy;
7. factual limits and avoid list.

Keep the shared brand signature out of generated artwork. Ask the image model to leave the reserved lower-left footer area open; composite [`assets/brand/learn-cs-with-us-lockup.svg`](../assets/brand/learn-cs-with-us-lockup.svg) onto the approved composition afterward. This preserves exact spelling, position, and styling across images.

## Reusable topic prompt

```text
Use case: scientific-educational infographic.
Audience: [A-level / university / software professional; prior knowledge].
Learning goal: [what the learner should understand or be able to do].
Main claim: [one sentence].

STYLE ANCHOR:
Paste the “Infographic prompt anchor” from docs/STYLE.md here without changing it.

TOPIC:
Explain [topic/mechanism]. Show [objects] and their relationships.
The sequence is: [numbered causal steps].
Worked example: [inputs, intermediate state, expected output].
Supporting details: [comparison, boundary case, misconception, use case,
or advanced note]. Keep each detail relevant to the main claim.

COMPOSITION:
Use a [portrait/landscape] [ratio] page. Make [the central mechanism] the main
visual. Place [supporting views] where they support the reading path. Vary the
scale of the details; avoid a regular grid of equal cards. Preserve enough
whitespace for labels to remain legible. Leave the reserved lower-left brand
signature area open and clear of other copy; the shared SVG is added after
image generation.

EXACT COPY:
Render these labels verbatim: [short, checked list of exact titles, labels,
values, units, and takeaway]. Do not add other text.

ACCURACY:
[state any teaching simplification, implementation variation, source-specific
assumption, or uncertainty]. Do not invent values, timings, dimensions, or steps.
```

## Style reference instruction

When the image-generation tool accepts reference images, attach one selected sample and add:

```text
Use Image 1 as a STYLE reference only. Carry over its palette roles, typography
hierarchy, linework, surface texture, illustration finish, and level of detail.
Do not copy its subject, labels, facts, diagram, or page layout. Build the new
composition from the current topic brief. Keep the shared style recognizable
while choosing the arrangement that best explains this topic.
```

Use one style reference at a time. A large mixed reference set can make the target less clear. If the image generator lacks separate style and composition controls, use the written style anchor and specify the new composition carefully.

## Iteration prompt

Make one significant change per edit. Name what must change and what must stay fixed.

```text
Keep the current topic facts, title, palette, typography roles, illustration
style, and overall reading order. Change only [one specific issue]. Preserve
all other labels and relationships exactly. Do not add text or new data.
```

## Quality review prompt

```text
Review this infographic against the attached content brief and style guide.
Report only evidenced issues, grouped as:
1. factual or numeric errors;
2. incorrect/misleading arrows, grouping, or causal relationships;
3. missing or misspelled exact labels;
4. hierarchy, density, or legibility problems;
5. differences from the shared style anchor.
For every issue, identify its location and propose one concrete correction.
Do not silently rewrite the content or claim a visual element is accurate just
because it looks plausible.
```

## Generation and review standard

- Use a short list of exact copy; keep longer explanation in captions or a separate text layer.
- Keep addresses, numeric values, symbols, and units literal in the prompt.
- Ask for no unsupported numbers or extra labels.
- Review every image manually against its sourced brief. Image generation is a visual production tool; it does not replace factual review.
- Use an output that follows the approved brand as a style reference; the written style guide remains the source of truth.
