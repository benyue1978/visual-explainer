# One Number, Three Bases — Image Prompt

Use case: scientific-educational infographic.
Asset type: Pinterest infographic with website use.
Audience: IGCSE and AS/A Level Computer Science learners who know denary place value and are learning binary and hexadecimal.
Learning goal: see how denary 173, binary 10101101, and hexadecimal AD represent the same value, and why four bits map to one hex digit.
Main claim: positional notation uses different place values in bases 10, 2, and 16; each group of four binary bits maps to one hexadecimal digit.

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
whitespace. Keep colors, typography roles, line language, footer signature, and
surface treatment recognizable across topics, while letting each topic have its
own metaphor, illustration, and composition.
Do not use generic dashboard grids, equal-sized cards, decoration without an explanatory role, neon,
purple gradients, fake technical labels, invented data, or tiny unreadable text.

TOPIC AND COMPOSITION:
Create the main artwork as a portrait 3:4 editorial technical infographic in the Visual CS series. The finished composition will receive a separate lower-left brand footer after generation, yielding an overall portrait page ratio of about 0.70 (width-to-height). The attached reference is for shared palette, expressive serif title, warm paper, linework, and illustration finish only. Do not copy its topic, diagrams, or composition.

Use a distinctive “number translation workbench” composition, not three equal cards. At the top, show a single large value 173 flowing into three equivalent forms. The familiar denary expression decomposes into one 100 tile, seven 10-rods, and three 1-dots; connect that to a long central binary place-value rail. Make the eight bit positions line up precisely over weights 128, 64, 32, 16 | 8, 4, 2, 1. Highlight active bits and their weights; subdued inactive bits contribute zero. At the lower half, reuse that exact same bit rail, bracket it into 1010 | 1101, then transform each four-bit group into one hex glyph: A and D. Show the value each group carries (10 and 13). Close with a bold equivalence and the idea that hex is a compact way to write the same binary value. The page should have one continuous scan path and a sense of transformation through layers, not a generic dashboard or equal-card grid.

EXACT COPY — render verbatim and preserve every value, order, and bit alignment:
Title: “173 in Denary, Binary & Hex”
“173₁₀ = 10101101₂ = AD₁₆”
“DENARY · BASE 10”
“1×100 + 7×10 + 3×1 = 173”
“BINARY · BASE 2”
“128  64  32  16  |  8  4  2  1”
“1    0   1   0   |  1  1  0  1”
“128 + 32 + 8 + 4 + 1 = 173”
“HEX · BASE 16”
“1010 | 1101”
“10 → A     13 → D”
“16 = 2⁴: one hex digit maps to four bits.”
“Different place values. Same value. Hex writes each four-bit group as one digit.”

ACCURACY AND AVOID:
The input is a non-negative integer represented by an 8-bit unsigned pattern. Denary expansion is 1×100 + 7×10 + 3×1. The selected binary weights 128 + 32 + 8 + 4 + 1 total 173. In base 16, A=10 and D=13, so AD=10×16+13=173. Align every bit above its correct power-of-two weight. Binary-to-hex groups are counted in fours from the right; because this example has exactly eight bits, the displayed groups read 1010 | 1101 from left to right. Do not change, reverse, duplicate, or reorder any bit. Do not imply A and D are text characters here. Do not add signed-number rules, arithmetic, BCD, ASCII, programming literal prefixes, a complete hex lookup table, syllabus labels, exam years, source citations, or any other text. Keep the lower-left footer safe area blank for the exact shared SVG, which will be composited afterward.
