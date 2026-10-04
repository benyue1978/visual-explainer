# One Number, Three Bases — Content Brief

- **Series position:** Third planned infographic in Data Representation
- **Audience:** IGCSE and AS/A Level Computer Science learners encountering number-base representation.
- **Prior knowledge:** Decimal place value, multiplication, and addition. Binary and hexadecimal are new or under development.
- **Terms to introduce:** denary (base 10), binary (base 2), hexadecimal/hex (base 16), place value, bit, hexadecimal digit.

## Learner question and purpose

- **Learner question:** How can the same value be written in denary, binary, and hexadecimal, and why can binary be grouped into hex digits?
- **Learning objective:** Explain that positional notation gives each digit a place value, verify that `173₁₀ = 10101101₂ = AD₁₆`, and show how each four-bit group maps to one hexadecimal digit.
- **Main claim:** Denary, binary, and hexadecimal are different positional notations for the same value; hexadecimal offers a direct, compact way to write binary because each hex digit represents exactly four bits.
- **Scope:** Positional place value in bases 10, 2, and 16; one conversion worked example; binary-to-hex grouping in four-bit groups; values A=10 and D=13.
- **Out of scope:** Signed integers, arithmetic operations, BCD, character codes, programming literal conventions such as `0x`, repeated-division conversion methods, and the full 0–F lookup table.
- **Module connection:** Representing Numbers; builds on bit patterns and prepares for interpreting fixed-width numeric representations.

## Concept model

1. **Object:** One non-negative integer written in three positional numeral systems.
2. **Denary:** Each digit is multiplied by a power of 10 according to its position: `173₁₀ = 1×10² + 7×10¹ + 3×10⁰ = 100 + 70 + 3`.
3. **Binary:** Each digit is multiplied by a power of 2: `10101101₂ = 1×128 + 0×64 + 1×32 + 0×16 + 1×8 + 1×4 + 0×2 + 1×1 = 173`.
4. **Hexadecimal:** Each digit is multiplied by a power of 16. `A` represents 10 and `D` represents 13, so `AD₁₆ = 10×16 + 13 = 173`.
5. **Binary-to-hex relationship:** Since `16 = 2⁴`, each hexadecimal digit maps to one group of four bits: `1010₂ = 10₁₀ = A₁₆`; `1101₂ = 13₁₀ = D₁₆`. Thus `1010 1101₂ = AD₁₆`.

## Worked example

- **Purpose:** One value can be checked through decimal place value, binary place values, and a direct four-bit-to-hex mapping.
- **Condition:** Use an 8-bit unsigned pattern. The example is an ordinary non-negative integer; no signed interpretation is implied.
- **Input:** Denary `173`.

| Step | Operation | Intermediate result | Interpretation |
|---|---|---|---|
| 1 | Expand denary digits by powers of 10 | `1×100 + 7×10 + 3×1` | `100 + 70 + 3 = 173` |
| 2 | Mark binary place values used by `10101101` | `128 + 32 + 8 + 4 + 1` | `173` |
| 3 | Split binary into four-bit groups | `1010 | 1101` | `10 | 13` |
| 4 | Replace each group with its hex digit | `A | D` | `AD₁₆` |

- **Final equivalence:** `173₁₀ = 10101101₂ = AD₁₆`.
- **Independent check:** `AD₁₆ = 10×16 + 13 = 160 + 13 = 173`; the binary selected place values also sum to 173.

## Supporting explanatory angles

- **Place-value view:** The three notations follow the same positional principle, but their place-value powers differ (10, 2, and 16).
- **Compactness view:** Hex is shorter to write than the same binary pattern because one hex digit corresponds to four bits. It is a human-readable notation for the same value, not a different stored quantity.
- **Symbol view:** `A` and `D` are hexadecimal digit symbols with values 10 and 13 in this example, not character codes or letters being encoded as text.

## Common misconceptions

| Misconception | Correction | Show it? |
|---|---|---|
| The binary and hex forms represent different values because their symbols look different. | Expand each using its place values; both yield 173. | Yes, show all three equivalent forms together. |
| `AD` is read as a denary number or as two text characters. | In base 16, `A=10` and `D=13`; place values give `10×16+13`. | Yes, label A and D with their numeric values. |
| A hex digit corresponds to one bit. | One hex digit corresponds to four bits because `16=2⁴`. | Yes, show `1010 | 1101` mapping to `A | D`. |

## Simplifications and implementation differences

- **Teaching model:** Treat all values as exact positional representations of one non-negative integer; show an 8-bit binary pattern for a readable example.
- **Limit:** The leading zeroes needed to pad a shorter binary number into four-bit groups do not change its value; this example already uses exactly eight bits, so padding is unnecessary.
- **Implementation differences:** None needed for this abstract conversion; programming-language literal prefixes are intentionally out of scope.

## Sources and derivations

| Claim | Basis | Source or derivation | Supports / limits |
|---|---|---|---|
| Digits in a base use place values that are powers of that base. | University teaching reference | [Princeton — Representing Information](https://introcs.cs.princeton.edu/java/61data/) | Explains positional number representation and base conversion; example values differ from this brief. |
| Four binary bits map to one hexadecimal digit because `16=2⁴`. | University course reference | [University of Chicago — Binary & Hex lecture notes](https://www.classes.cs.uchicago.edu/current/14300-1/lectures/lec03_notes/) | Directly supports four-bit grouping and hex digits A–F; example values differ from this brief. |
| `173₁₀ = 10101101₂ = AD₁₆`. | Transparent derivation | `1×100+7×10+3=173`; selected binary place values sum to 173; `10×16+13=173`. | Arithmetic recomputed; notation follows the cited base-conversion explanations. |

## Content review

**Status:** READY

**Reviewer:** Independent AI reviewer; calculations also recomputed manually.

**Findings and evidence:** Denary decomposition sums to `173`; binary selected place values sum to `128+32+8+4+1=173`; hexadecimal expansion is `10×16+13=173`. `16=2⁴` justifies the four-bit mapping. The example supports the central claim from complementary angles; A/D are explicitly treated as hexadecimal digit values, and the fixed 8-bit condition avoids signed-number ambiguity.

**Corrections made:** None after review.

- [x] One clear learner outcome and a complete worked example.
- [x] Important claims are sourced or transparently derived.
- [x] Number bases and symbols are distinguished; binary-to-hex grouping is explicit.
- [x] The example avoids implying signed interpretation or text encoding.
- [x] Supporting angles deepen the same question without introducing a separate lesson.
- [x] Learner-facing art contains no syllabus names, codes, years, or coverage labels.
