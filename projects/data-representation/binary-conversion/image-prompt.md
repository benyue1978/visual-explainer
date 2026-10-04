# Image Production Notes — Binary ↔ Denary

## Production method

Build the composition as editable SVG, then render the PNG from that source. The exact arithmetic and six aligned position labels require deterministic typesetting. Preserve the approved palette, editorial serif heading, monospaced arithmetic, fine vector-like linework, restrained paper texture, asymmetric reading path, and shared lower-left brand lockup.

## Style anchor

```text
Create a polished editorial technical field guide in a relaxed, trustworthy,
professionally art-directed visual style. Use a warm ivory paper canvas, a quiet
low-saturation base, and the shared semantic palette: deep blue-black for type
and outlines, muted slate for structures, dusty teal for inputs and active paths,
muted copper for values and results, and soft coral for warnings or control
signals. Use precise vector-like diagrams, clean silhouettes, fine consistent
linework, restrained paper grain, and occasional fine hatching. Use an expressive
editorial serif for the main title, legible compact labels, and monospaced type
for code, addresses, and formulas. Build an asymmetric page around one dominant
annotated mechanism diagram, then add two to five topic-relevant supporting
details with a clear reading path. Make the page rich but orderly, with deliberate
whitespace. Keep colors, typography roles, line language, footer signature, and
surface treatment recognizable across topics, while letting each topic have its
own metaphor, illustration, and composition.
Do not use generic dashboard grids, equal-sized cards, decoration without an explanatory role, neon,
purple gradients, fake technical labels, invented data, or tiny unreadable text.
```

## Composition requirements

- Portrait canvas 1086×1556, warm ivory paper.
- The title names the actual topic: `Binary ↔ Denary: How to Convert`.
- Put the shared value pair `53₁₀ = 110101₂` high on the page.
- Upper method: align exponents `2⁵ 2⁴ 2³ 2² 2¹ 2⁰`, place values `32 16 8 4 2 1`, bits `1 1 0 1 0 1`, and contributions `32 16 0 4 0 1`. Let the active weights flow into `32 + 16 + 4 + 1 = 53`.
- Lower method: show exactly six repeated division equations, through quotient zero. Put one circled remainder value (`1, 0, 1, 0, 1, 1` from top to bottom) alongside each equation; do not add `r0`/`r1` prefixes or a vertical divider. Make the upward reading direction unmistakable; reveal `110101₂`.
- Add a concise verification cue and boundary note `0₁₀ = 0₂`.
- Composite the exact SVG lockup `assets/brand/learn-cs-with-us-lockup.svg` in the lower-left footer. Do not redraw or paraphrase it.
- Keep all arithmetic and labels large enough for phone viewing. Add no syllabus/exam labels, unsupported numbers, extra examples, or filler text.
