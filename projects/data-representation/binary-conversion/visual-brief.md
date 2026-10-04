# Binary ↔ Denary: How to Convert — Visual Brief

## Audience and learning purpose

- **Audience / prior knowledge:** IGCSE and AS/A Level Computer Science learners who know denary place value and integer division with remainders.
- **Learner question:** How do I convert a whole number from binary to denary, and from denary to binary?
- **Learning objective:** Read binary place values to find a denary value; convert a positive denary integer into binary by repeated division and bottom-up remainder reading.
- **Main claim:** Binary-to-denary adds the place values selected by 1-bits; denary-to-binary repeatedly divides by 2 and reads the remainders upwards.

## Scope and concept coverage

- **Core mechanism:** Two complementary procedures connected by the same equality, `53₁₀ = 110101₂`.
- **In scope:** All six binary positions and contributions; all six division steps through quotient 0; upward remainder order; final equivalence; compact zero boundary `0₁₀ = 0₂`.
- **Out of scope:** Fractions, negative numbers, signed/fixed-width patterns, hexadecimal, other bases, programming notation, syllabus/exam labels.
- **Accuracy assumptions / simplifications:** Ordinary positional notation; positive whole number in the worked repeated-division example. Subscripts identify the base. `0` is shown as a separate boundary case rather than forced through the longer example.

## Reading path

1. Read the title and see the shared target pair `53₁₀ ↔ 110101₂`.
2. Follow the upper path from `110101₂` to denary: align the bits with `32,16,8,4,2,1`, illuminate contributions from 1-bits, then sum to 53.
3. Follow the lower path from `53₁₀` through six divisions by 2; each quotient becomes the next dividend and each remainder is recorded.
4. Follow a visually unmistakable upward arrow through the remainders to assemble `110101₂`.
5. Close with the equality as a cross-check and a brief takeaway; include `0₁₀ = 0₂` as a quiet boundary note.

## Visual structure

- **Hero visual:** A two-way conversion workbench built around one large equality. The number itself is the shared anchor; two distinct process paths show how to move in each direction.
- **Selected supporting views:**
  - A six-position binary place-value rail. Each bit sits directly above its weight; selected weights flow into a sum tray while zero-bit positions stay visible but quiet.
  - A descending quotient staircase for repeated division, with a narrow remainder column. An upward return arrow follows the remainder column to form the binary answer.
  - A small verification link points from the final binary result back to the place-value sum; this shows how to check the conversion independently.
- **Purpose of each support:** The place-value rail makes bit alignment and contribution explicit; the quotient staircase exposes the state change at each division; the upward trail prevents reversing the remainders incorrectly; the return link models answer checking.
- **Analogy mapping and limit:** Use an illustrated place-value rack and a paper calculation staircase as visual metaphors for the procedures. They represent mathematical steps, not physical computer hardware or a machine's literal internals.
- **Composition / scan path:** Portrait, asymmetric editorial page. A clear title and shared number pair lead into the first method in the upper half. A sweeping connector hands the result 53 into the lower division path. Make the quotient chain descend, but make the remainder-reading arrow rise, using separate colors/line styles so the opposite directions cannot be confused. End with a large answer pair and a short memory cue. Avoid two equal generic cards; let the long remainder staircase use more vertical room.
- **Canvas and expected viewing size:** Warm ivory, portrait page approximately 1086×1556 (about 0.70 width-to-height), matching the finished number-bases infographic. Prioritize phone-scale legibility for division rows and instructions; exact equations should be editable vector text.
- **Brand safe area:** Keep the bottom-left footer area open and composite the exact `assets/brand/learn-cs-with-us-lockup.svg` as the final vector layer.

## Exact learner-facing copy

- **Title:** `Binary ↔ Denary: How to Convert` (may wrap across two lines but must remain verbatim)
- **Subtitle:** `Two methods. One value.` (sentence case, verbatim)
- **Shared example:** `53₁₀ = 110101₂`
- **Method 1 heading:** `BINARY → DENARY`
- **Method 1 cue:** `Each 1 adds its place value. Each 0 adds zero.`
- **Place values, left to right:** `32  16  8  4  2  1`
- **Position labels, left to right:** `2⁵  2⁴  2³  2²  2¹  2⁰`
- **Bits:** `1   1   0  1  0  1`
- **Contributions:** `32  16  0  4  0  1`
- **Sum:** `32 + 16 + 4 + 1 = 53`
- **Method 2 heading:** `DENARY → BINARY`
- **Method 2 cue:** `Divide by 2. Continue with each quotient until it is 0.`
- **Division rows:**
  - `53 ÷ 2 = 26`
  - `26 ÷ 2 = 13`
  - `13 ÷ 2 = 6`
  - `6 ÷ 2 = 3`
  - `3 ÷ 2 = 1`
  - `1 ÷ 2 = 0`
- **Remainder markers, top to bottom:** circled `1, 0, 1, 0, 1, 1`, aligned one-to-one with the divisions; do not prefix them with `r` or add a separating vertical rule.
- **Remainder direction:** `READ REMAINDERS UP`
- **Result:** `110101₂`
- **Check:** `32 + 16 + 4 + 1 = 53`
- **Boundary note:** `0₁₀ = 0₂`
- **Takeaway:** `Binary → add the selected powers of 2. Denary → divide by 2; read remainders upwards.`

## Visual brief review

- **Status:** READY
- **Reviewer:** Independent AI reviewer.
- **Findings and evidence:** Independent re-review of the final PNG verified that all six circled remainder values align with their corresponding division rows in the order `1,0,1,0,1,1`. The header sits over that column, the upward arrow and `BOTTOM TO TOP` label make the reading direction clear, and the result appears at the return-line endpoint. No overlaps or spacing issues were introduced.
- **Corrections made:** Added position labels `2⁵` through `2⁰`; made the title and subtitle verbatim, increased instructional/equation sizes, removed an overflowing label, and separated the reverse-check text from its equation. On user direction, removed the vertical divider and `r0`/`r1` text, placing only the circled remainder values in the remainder column.
