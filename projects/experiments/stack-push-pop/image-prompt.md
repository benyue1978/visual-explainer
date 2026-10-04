# Image-generation prompt · stack push and pop

Style anchor: `docs/STYLE.md` v1.0.
Topic source: `content-brief.md`.  
Composition: `visual-brief.md`.

```text
Use case: scientific-educational infographic.
Audience: A-level and introductory university computer science learners.
Learning goal: follow push, pop, and peek operations and predict which value is returned.
Main claim: a stack adds and removes items at its top, so the last item pushed is the first item popped.

STYLE ANCHOR:
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
whitespace. Keep colors, typography roles, line language, and surface treatment
recognizable across topics, while letting each topic have its own composition.
Do not use generic dashboard grids, equal-sized cards, decorative filler, neon,
purple gradients, fake technical labels, invented data, or tiny unreadable text.

TOPIC:
Show a tall stack of values with TOP clearly marked. Show this exact state trace:
push 12, then push 7, then pop returns 7, then push 5. Keep 12 below 7 before
the pop; show 7 leaving from the top; after the last push show 12 below 5.
Add one small operation key for PUSH, POP, and PEEK; PEEK leaves the top item
in place. Add compact edge-case notes for popping an empty stack (underflow)
and overflowing a fixed-capacity stack. A small inset may show nested function
calls returning in reverse order. Do not confuse the abstract stack rule with
one physical implementation.

COMPOSITION:
Portrait 4:5 page. Give the stack and its changing states the main visual weight.
Use a connected four-state sequence rather than equal cards. Add a narrow inset
for PEEK, a compact underflow/overflow boundary note, and one small call-stack
application illustration. Use leader lines and varied scale; keep the scan path
clear and allow the page to reward close reading.

EXACT COPY:
“Stack: push and pop”
“The top is the only doorway.”
“Last in, first out (LIFO)”
“PUSH adds to the top.”
“POP removes and returns the top.”
“PEEK reads the top; it stays there.”
“push 12 → push 7 → pop returns 7 → push 5”
“UNDERFLOW: pop an empty stack”
“OVERFLOW: only when a fixed capacity is full”
“Array or linked nodes: same stack behavior”
“Nested calls return in reverse order.”
“Add and remove at one end: the TOP.”
Render the listed words, values, and symbols exactly. Add no other text.

ACCURACY:
Stack operations affect only the top. The example ends with 12 at the bottom
and 5 at the top. Overflow applies here only to a fixed-capacity implementation;
a growable stack may resize. Do not add numeric performance claims or a capacity.
No logo or watermark.
```
