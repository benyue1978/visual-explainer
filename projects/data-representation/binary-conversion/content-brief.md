# Converting Between Binary and Denary — Content Brief

- **Series position:** Next planned infographic after `173 in Denary, Binary & Hex`.
- **Audience:** IGCSE and AS/A Level Computer Science learners who need to convert whole numbers between denary and binary.
- **Prior knowledge:** Denary place value, powers, multiplication/addition, and integer division with remainders.
- **Terms to introduce:** denary (base 10), binary (base 2), place value (the value assigned to a digit's position), quotient (the whole-number result of division), remainder (what is left after taking the whole-number quotient).

## Learner question and purpose

- **Learner question:** Given a binary whole number, how do I find its denary value—and how do I turn a denary whole number into binary?
- **Learning objective:** Use binary place values to convert binary to denary, and repeated division by 2 with bottom-up remainders to convert denary to binary.
- **Main claim:** The two directions use complementary methods: add the powers of 2 selected by the 1-bits, or repeatedly divide by 2 and read the remainders from bottom to top.

## Scope

- **In scope:** The two conversion procedures for non-negative whole numbers; one shared, fully worked example; an independent reverse check.
- **Out of scope:** Fractions, negative numbers, signed or fixed-width interpretation, hexadecimal, other bases, and programming notation.
- **Module connection:** Representing Numbers; follows the place-value and number-base equivalence example in `number-bases/` by teaching a reusable conversion procedure.

## Concept model

1. **Binary to denary:** A binary digit at position `n` contributes `bit × 2ⁿ`. Start with position 0 at the right; a 1 contributes that place value and a 0 contributes zero. Add the contributions.
2. **Denary to binary:** Divide the denary integer by 2. Keep each quotient for the next division and record each remainder. Stop when the quotient is 0. The first remainder is the least significant bit, so read the remainders in reverse order (bottom to top) to form the binary numeral.
3. **Verification:** Convert the resulting binary numeral back by summing its selected powers of 2. The result should equal the starting denary integer.

## Worked example

- **Purpose:** Use one number in both directions so each algorithm is visible and the result can be checked independently.
- **Conditions:** Positive whole number for the worked procedure; ordinary positional notation, with no signed or fixed-width interpretation. Zero is a simple boundary case: `0₁₀ = 0₂`.
- **Input pair:** `110101₂` and `53₁₀`.

### Binary to denary

| Position value | 32 | 16 | 8 | 4 | 2 | 1 |
|---|---:|---:|---:|---:|---:|---:|
| Bit in `110101₂` | 1 | 1 | 0 | 1 | 0 | 1 |
| Contribution | 32 | 16 | 0 | 4 | 0 | 1 |

`110101₂ = 1×32 + 1×16 + 0×8 + 1×4 + 0×2 + 1×1 = 53₁₀`

### Denary to binary

| Division | Quotient | Remainder |
|---|---:|---:|
| `53 ÷ 2` | 26 | 1 |
| `26 ÷ 2` | 13 | 0 |
| `13 ÷ 2` | 6 | 1 |
| `6 ÷ 2` | 3 | 0 |
| `3 ÷ 2` | 1 | 1 |
| `1 ÷ 2` | 0 | 1 |

Read the remainders bottom to top: `110101₂`. Therefore `53₁₀ = 110101₂`.

- **Cross-check:** `32 + 16 + 4 + 1 = 53`.

## Explanatory depth

- Align every bit with its power-of-two place value; label the rightmost place `2⁰ = 1` so the direction of counting positions is clear.
- Make the remainder reading direction visible, since reading top to bottom gives the wrong result. A vertical remainder trail with an upward reading arrow can make this procedural reversal memorable.
- The two methods are complementary views of the same place-value system: one expands a numeral into powers of 2; the other constructs its bits from successive remainders.
- Show a reverse-check link between the two worked paths so the learner sees how to catch an answer error.

## Common misconceptions

| Misconception | Correction | Show it? |
|---|---|---|
| Read binary digits as a denary number made only of 0s and 1s. | Multiply each bit by its aligned power-of-two place value and add. | Yes, explicitly align bits and place values. |
| Start place values at `2¹` on the right. | The rightmost position is `2⁰ = 1`; positions increase moving left. | Yes, label all place values for the example. |
| Read division remainders in the order they were produced. | The earliest remainder is the rightmost/least significant bit; read the list bottom to top. | Yes, use a clear upward arrow and final numeral. |
| Stop division while the quotient is still positive. | Continue until the quotient becomes 0; the last non-zero quotient step contributes the leftmost bit. | Yes, include the final `1 ÷ 2 = 0 r1` row. |

## Teaching model and limitations

- **Teaching model:** These are exact procedures for non-negative integers in ordinary base-2/base-10 notation.
- **Limit:** The example does not address negative values or fractions; those require additional representation rules or steps.
- **Implementation differences:** None for the abstract conversion shown.

## Sources and derivations

| Claim | Basis | Source or derivation | Supports / limits |
|---|---|---|---|
| Binary digits represent a sum of powers of 2, one contribution per bit position. | University teaching reference | [Princeton — Representing Information, Binary and hexadecimal](https://introcs.cs.princeton.edu/java/61data/#) | Defines binary positional notation and illustrates conversion by powers of 2. |
| To convert a denary integer to base 2, repeatedly divide by 2 and read remainders upwards. | University teaching reference | [Princeton — Representing Information, Number conversion](https://introcs.cs.princeton.edu/java/61data/#) | Explicitly describes repeated division by the target base and bottom-up remainder reading. |
| `110101₂ = 53₁₀`. | Transparent derivation | `1×32 + 1×16 + 0×8 + 1×4 + 0×2 + 1×1 = 53`. | Exact arithmetic from the binary place-value rule. |
| `53₁₀ = 110101₂`. | Transparent derivation | Repeated divisions yield remainders top-down `1,0,1,0,1,1`; reverse to `110101`. | Exact arithmetic from the repeated-division rule. |

## Content review

**Status:** READY

**Reviewer:** Independent AI reviewer; calculations recomputed separately.

**Findings and evidence:** The reviewer verified the binary expansion (`32+16+4+1=53`) and repeated divisions (`53,26,13,6,3,1,0` with remainders `1,0,1,0,1,1`, read in reverse). Princeton directly supports binary place values as powers of two and repeated division by the target base with remainders read upwards. The reviewer requested scope consistency and learner-facing explanations of quotient and remainder.

**Corrections made:** Clarified that the worked procedure uses a positive whole number, noted zero as a boundary case, and added short first-use definitions for place value, quotient, and remainder. No arithmetic or scope blockers remain.
