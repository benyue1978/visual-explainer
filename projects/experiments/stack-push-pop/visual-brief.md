# Visual brief: stack push and pop

Use the approved visual style in `docs/STYLE.md`. This is an introductory data-structure topic.

## Visual thesis

The only working end is the top; each push changes that end, and each pop returns the latest item.

## Composition

- Portrait 4:5 page with the fixed editorial technical field-guide treatment.
- Large central stack illustration, shown at the start and after each operation in a short state trace.
- Clearly mark TOP; use an incoming teal value for push and a copper value leaving for pop.
- Use the worked example `push 12 → push 7 → pop returns 7 → push 5` with four small, connected state changes.
- Add a compact operation key for PUSH / POP / PEEK; a bottom comparison for underflow versus bounded-capacity overflow; and a small call-stack application note.
- Maintain the shared style and detail level while using a composition suited to a simple state-change concept.

## Required checks

- Show `12` beneath `7` before the pop, and show `7` leaving the top.
- After `push 5`, the stack contains `12` at the bottom and `5` at the top.
- PEEK leaves the stack unchanged.
- Explain that overflow depends on a fixed-capacity implementation.
- Keep the call-stack application as a related use, not the definition of the stack ADT.
