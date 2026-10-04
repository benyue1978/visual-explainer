# Data Size Prefixes — Content Brief

- **Status:** Reviewed and ready for visual planning
- **Series position:** Second planned infographic in Data Representation
- **Audience:** IGCSE and AS/A Level Computer Science learners encountering storage units and binary prefixes.
- **Prior knowledge:** A byte contains 8 bits; learners can read multiplication and powers of ten. No prior knowledge of binary prefixes is assumed.

## Learner question and purpose

- **Learner question:** Why do `kB` and `KiB` represent different numbers of bytes, and how does the difference continue at larger units?
- **Learning objective:** Explain that SI prefixes such as kilo and mega are decimal powers, while IEC prefixes such as kibi and mebi are binary powers; calculate the exact byte counts for `1 kB`, `1 KiB`, `1 MB`, and `1 MiB`.
- **Main claim:** Decimal prefixes scale by powers of 1,000, while binary prefixes scale by powers of 1,024; the distinction is shown explicitly by `kB` versus `KiB` and `MB` versus `MiB`.
- **Scope:** Explain prefix meaning through kilo/kibi and mega/mebi, exact byte counts, and the resulting difference at the mega level.
- **Out of scope:** Storage-device marketing, operating-system display conventions, historical reasons for the old ambiguity, converting arbitrary file sizes, bits per second, and prefixes beyond mega/mebi.

## Concept model

1. **Quantity:** byte (`B`). In the examples below, all totals are bytes.
2. **Decimal family:** `k = 10^3 = 1,000`; `M = 10^6 = 1,000,000`. Therefore `1 kB = 1,000 B`, and `1 MB = 1,000 kB = 1,000,000 B`.
3. **Binary family:** `Ki = 2^10 = 1,024`; `Mi = 2^20 = 1,048,576`. Therefore `1 KiB = 1,024 B`, and `1 MiB = 1,024 KiB = 1,048,576 B`.
4. **Contrast:** `1 MiB − 1 MB = 1,048,576 − 1,000,000 = 48,576 bytes`.
5. **Notation cue:** Prefix capitalization and spelling matter: SI `k` is lowercase, `M` is uppercase; binary prefixes use `Ki` and `Mi`. `B` denotes byte.

## Worked example

Compare one megabyte with one mebibyte:

- Decimal path: `1 MB = 1,000 kB = 1,000 × 1,000 B = 1,000,000 B`.
- Binary path: `1 MiB = 1,024 KiB = 1,024 × 1,024 B = 1,048,576 B`.
- Difference: `48,576 B`.

These are exact prefix definitions, not measurements of a particular file or drive. The visual should present both counts directly and must not use bar lengths or areas that imply an exaggerated proportional difference.

## Supporting explanatory angles

- **Parallel paths:** Two clearly named ladders share a `1 byte` starting point. Decimal steps multiply by `1,000`; binary steps multiply by `1,024`. This shows the rule behind the names rather than asking learners to memorize four isolated values.
- **Notation comparison:** `kB` and `KiB` differ by spelling and case as well as value; `MB` and `MiB` continue their respective families.
- **Scale detail:** The step difference becomes `48,576 bytes` at the mega/mebi level. State the subtraction so this is a derived comparison, not an unexplained fact.

## Misconceptions and boundaries

- Do not equate `kB` with `KiB` or `MB` with `MiB`.
- Do not write `KB` as the decimal kilobyte symbol; use `kB`.
- Do not suggest the decimal and binary prefixes are interchangeable or that a specific software display must use one convention.
- Keep byte (`B`) distinct from bit (`b`); this piece's equations are all in bytes.
- Avoid historical explanation: the learner needs the definitions and how to read them.

## Sources

- [BIPM — SI prefixes](https://www.bipm.org/en/measurement-units/si-prefixes): SI decimal prefixes; kilo (`k`) is `10^3`, mega (`M`) is `10^6`.
- [NIST — Definitions of the SI units: The binary prefixes](https://physics.nist.gov/cuu/Units/binary.html): IEC binary prefix names and symbols; `Ki = 2^10`, `Mi = 2^20`; examples for byte multiples.
- [NIST — Guide to the SI, Chapter 4](https://www.nist.gov/pml/special-publication-811/nist-guide-si-chapter-4-two-classes-si-units-and-si-prefixes): SI prefixes denote powers of ten and should not be used to indicate powers of two.

## Content review

- **Status:** READY
- **Reviewer:** Independent content review pass
- **Findings:** Definitions and symbols agree with BIPM and NIST references. Multiplications and subtraction were recomputed. Scope is focused on interpreting prefix families; useful depth is provided by the paired ladder, exact values, notation cue, and explicit difference. The visual must avoid proportional bars that magnify a 4.8576% difference.
- **Corrections made:** Used exact SI casing (`kB`, `MB`) and IEC binary forms (`KiB`, `MiB`); added the exact `48,576 B` derivation and the visual-scale caveat.
