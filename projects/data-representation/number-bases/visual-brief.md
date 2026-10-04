# One Number, Three Bases — Visual Brief

## Audience and learning purpose

- **Audience / prior knowledge:** IGCSE and AS/A Level Computer Science learners; know decimal place value, learning binary and hex.
- **Learner question:** How can denary, binary, and hexadecimal show the same value?
- **Learning objective:** Verify `173₁₀ = 10101101₂ = AD₁₆` and explain the four-bit grouping that connects binary to hex.
- **Main claim:** The three forms use different place-value bases but represent the same quantity; one hex digit maps exactly to four bits.

## Scope and concept coverage

- **Core mechanism:** Decode each positional notation using powers of its base; group the binary sequence into nibbles and map each nibble to one hex digit.
- **In scope:** Denary decomposition `100+70+3`; binary weights `128,64,32,16,8,4,2,1`; selected-bit sum `128+32+8+4+1`; groups `1010|1101`, counted in fours from the right (for this eight-bit example, the split falls between the two nibbles); mapping `10→A`, `13→D`; final equivalence.
- **Out of scope:** Signed numbers, arithmetic operations, BCD, character encoding, programming notation such as `0x`, full lookup tables, syllabus or exam references.
- **Accuracy assumptions:** 8-bit unsigned example. Use base subscripts or clear base labels. No other number can be confused with a count of objects or a character code.

## Reading path

1. See the same value `173` named in three notations: `173₁₀`, `10101101₂`, `AD₁₆`.
2. Unpack the familiar denary number into `1×100 + 7×10 + 3×1`.
3. Trace the binary digits over place values `128` down to `1`; illuminate only the selected weights and sum to 173.
4. Reuse the exact same eight-bit strip, split into `1010 | 1101`.
5. Map each four-bit group to a hex digit: `1010 = 10 = A`; `1101 = 13 = D`.
6. Close with `16 = 2⁴` and the takeaway that hex is compact notation for the same binary value.

## Visual structure

- **Hero visual:** One long, horizontal 8-bit place-value instrument (128 to 1), with active bits highlighted as raised copper tiles and inactive bits recessed in slate. The binary value should remain the main diagram, not a generic comparison card.
- **Selected supporting views:** Denary place-value decomposition above the bit instrument, visualized as one 100 tile, seven 10-rods, and three 1-units; below it, a magnified split of the same binary strip into two four-bit groups that transform into `A` and `D`.
- **Purpose of supports:** Denary decomposition connects the new notation to familiar base-10 place value; the paired nibble mapping makes the binary-to-hex relationship concrete and explains why the hex form is shorter.
- **Analogy mapping and limit:** Treat the bit instrument as a place-value ruler: a lit bit contributes its labeled weight, an unlit bit contributes zero. It illustrates positional value, not physical storage components.
- **Composition / scan path:** Portrait composition. Editorial title and large equivalence headline. Denary line feeds into the 8-bit place-value instrument. The same bit strip then visually folds into two nibble windows and resolves into `AD`. Use a clear, directional transformation rather than three equal cards. A small total line verifies `128+32+8+4+1=173`; a bottom takeaway explains compactness.
- **Canvas and expected viewing size:** Warm ivory paper. Generate the main composition at portrait 3:4, then extend the bottom with the shared publisher footer; final delivered canvas is approximately 0.70 width-to-height (1086×1556), matching the preceding series artwork. Keep formulas large and use monospaced digits for Pinterest phone viewing.
- **Brand safe area:** Reserve the lower-left footer region for the exact shared SVG signature.

## Exact learner-facing copy

- **Title:** `173 in Denary, Binary & Hex`
- **Main equivalence:** `173₁₀ = 10101101₂ = AD₁₆`
- **Labels / values:**
  - `DENARY · BASE 10`
  - `1×100 + 7×10 + 3×1 = 173`
  - `BINARY · BASE 2`
  - `128  64  32  16  |  8  4  2  1`
  - `1    0   1   0   |  1  1  0  1`
  - `128 + 32 + 8 + 4 + 1 = 173`
  - `HEX · BASE 16`
  - `1010 | 1101`
  - `10 → A     13 → D`
  - `16 = 2⁴: one hex digit maps to four bits.`
- **Takeaway:** `Different place values. Same value. Hex writes each four-bit group as one digit.`

## Visual brief review

- **Status:** READY
- **Reviewer:** Independent AI review against the READY content brief
- **Findings and evidence:** Preserves the full worked example and all three complementary views. The same binary strip is reused so the four-bit grouping is visibly connected to the binary value, not introduced as a second unrelated example. The decimal decomposition grounds the new systems in familiar place value. The denary tile/rod/dot drawing is an illustration of `100+70+3`, not a new counting lesson. The labels fit the final portrait canvas at readable size.
- **Corrections made:** Recorded the final approximately 0.70 canvas ratio after adding the series footer; this matches the preceding Data Representation artwork.
