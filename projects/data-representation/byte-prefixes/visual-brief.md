# Data Size Prefixes — Visual Brief

## Audience and learning purpose

- **Audience / prior knowledge:** IGCSE and AS/A Level Computer Science learners; know bytes and multiplication, new to IEC binary prefixes.
- **Learner question:** Why do `kB` and `KiB` represent different byte counts?
- **Learning objective:** Follow decimal and binary prefix steps and compare their exact mega-level results.
- **Main claim:** `kB`/`MB` scale by 1,000; `KiB`/`MiB` scale by 1,024.

## Scope and concept coverage

- **Core mechanism:** Two multiplicative prefix ladders start from one byte and diverge: decimal ×1,000 per prefix step; binary ×1,024 per prefix step, with `2^10 = 1,024` explaining the binary factor.
- **In scope:** `1 kB = 1,000 B`; `1 KiB = 1,024 B`; `1 MB = 1,000,000 B`; `1 MiB = 1,048,576 B`; difference `48,576 B`.
- **Out of scope:** History, storage-device claims, computer display conventions, beyond-mega prefixes, bits per second.
- **Accuracy assumptions / simplifications:** All displayed quantities are exact byte counts. Do not encode quantities with visually exaggerated bar lengths; diagram positions are schematic.

## Reading path

1. Start at one shared byte marker.
2. Follow two diverging editorial staircases, labeled decimal and binary.
3. Read the per-step multiplier and exact kilo-level value.
4. Follow each staircase one more step to MB or MiB and its exact byte total.
5. Compare the totals in a shared, magnified difference annotation: `48,576 bytes more in 1 MiB than in 1 MB`.
6. End with a compact notation reminder: `1 kB = 1,000 B; 1 MB = 1,000 kB` and `1 KiB = 1,024 B; 1 MiB = 1,024 KiB`; uppercase/lowercase and the `i` matter.

## Visual structure

- **Hero visual:** Two topic-specific staircases emerge from one small `1 byte` origin. Label both decimal jumps ×1,000. Label both binary jumps ×1,024, and connect them to one shared formula key, `2^10 = 1,024`, which defines each binary prefix jump. Do not depict one thousand twenty-four individual byte blocks. Use restrained, clear labels so the metaphor supports rather than replaces exact numbers.
- **Selected supporting views:** Exact worked comparison at MB/MiB; a direct notation comparison embedded in the title and the paired unit labels on the two paths (`kB`/`KiB`, then `MB`/`MiB`).
- **Purpose of each support:** Exact calculations make the distinction verifiable; seeing each decimal/binary pair in matching positions helps learners decode the prefix spelling and capitalization.
- **Analogy mapping and limit:** Stair steps represent repeated multiplication by each prefix factor. They are a conceptual path, not proportional measures; do not imply a unit step is a physical or equal-sized block count.
- **Composition / scan path:** Portrait 3:4. Large editorial title already juxtaposes `kB`/`KiB` and `MB`/`MiB`. A single shared origin near upper middle splits into two asymmetrical, color-coded paths that move down and outward; corresponding units occupy matching levels. Put exact counts beside each step. Place the binary rule key beside the binary path, using its copper color and direct label; each binary arrow is separately labeled `× 1,024`. Do not connect the formula back to the shared origin. A lower inset compares the mega-level totals numerically rather than with unequal area bars. Use no regular equal-card grid.
- **Canvas and expected viewing size:** Warm ivory paper, portrait 3:4, intended to remain readable as a Pinterest pin on a phone.
- **Brand safe area:** Reserve lower-left footer space for the exact shared SVG lockup.

## Exact learner-facing copy

- **Title:** `Data Size Prefixes: kB vs KiB, MB vs MiB`
- **Labels / values:**
  - `DECIMAL` / `× 1,000 each step`
  - `One binary prefix step: 2^10 = 1,024`
  - `1 kB = 1,000 bytes`
  - `1 MB = 1,000 kB = 1,000,000 bytes`
  - `BINARY` / `× 1,024 each step`
  - `1 KiB = 1,024 bytes`
  - `1 MiB = 1,024 KiB = 1,048,576 bytes`
  - `1 MiB is 48,576 bytes more than 1 MB`
  - `B = byte`
  - `The letter i matters: KiB and MiB use powers of 2.`
- **Takeaway:** `Read the prefix: kB and KiB are different amounts.`

## Visual brief review

- **Status:** READY
- **Reviewer:** Independent visual-brief review against the reviewed content brief
- **Findings and evidence:** Includes every in-scope definition and the worked mega/mebi comparison. Paired paths visually encode the different repeated factors; exact values stay adjacent to their paths. Prefix spelling is contrasted in both the title and the aligned path labels. The stair metaphor's limit is explicit, and comparison is numeric to avoid misleading scale. No syllabus or historical material appears.
- **Corrections made:** Replaced ambiguous binary counting marks with a shared formula key showing `2^10 = 1,024` and made it explicit that each binary jump uses this factor. Corrected the prefix memory cue so it distinguishes each kilo-to-mega step accurately. Removed the requirement for a separate letterform inset because the paired symbols are directly contrasted in the title and paths. Added a warning against proportional bars and an instruction not to point the binary rule back to the shared origin.
