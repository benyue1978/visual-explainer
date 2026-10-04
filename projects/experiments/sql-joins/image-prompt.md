# Image-generation prompt · SQL joins

Style anchor: `docs/STYLE.md` v1.0.
Style reference: `projects/experiments/stack-push-pop/assets/stack-push-pop.png` — style only; do not copy its stack subject or state-trace layout.
Topic source: `content-brief.md`.  
Composition: `visual-brief.md`.

```text
Use case: scientific-educational infographic.
Audience: A-level, university, and early-career software learners.
Learning goal: predict which rows appear in INNER, LEFT, and FULL OUTER joins.
Main claim: the ON condition pairs matching rows; join type controls which unmatched rows remain.

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

STYLE REFERENCE:
Use Image 1 as a STYLE reference only. Carry over its palette roles, typography
hierarchy, linework, surface texture, illustration finish, and level of detail.
Do not copy its stack subject, values, labels, diagram, or page layout. Build a
new relational table illustration with a different composition.

TOPIC:
Two source tables meet on the key customer_id. Use these exact rows.
Use source columns Orders(order_id, customer_id) and
Customers(customer_id, customer_name). Use result columns order_id and
customer_name.
Orders: (101, C1), (102, C2), (103, C4).
Customers: (C1, Mina), (C2, Ravi), (C3, Jo).
Show the exact join condition Orders.customer_id = Customers.customer_id.
INNER output: (101, Mina), (102, Ravi).
LEFT output: those two rows plus (103, NULL), because C4 has no customer match.
FULL OUTER output: the LEFT rows plus (NULL, Jo), because C3 has no order match.
Show that duplicate keys can multiply result rows in one small inset.

COMPOSITION:
Portrait 4:5 page. Center a strong visual of the two tables meeting on matching
keys, with teal highlighting matching IDs and copper marking output rows. Around
it show three result views—INNER, LEFT, FULL OUTER—with the unmatched C4 and C3
rows visually traced into the appropriate results. Use fine leader lines rather
than a Venn diagram. Add a compact duplicate-key inset and a small NULL note.
Vary the scale of the detail; keep the scan path clear and typography legible.

EXACT COPY:
“SQL joins: match keys, shape rows”
“JOIN rows when ON is true.”
“INNER: matched pairs only”
“LEFT: every left row + matches”
“FULL OUTER: every row from both sides”
“No match? Missing-side columns become NULL.”
“Duplicate keys can multiply result rows.”
“Orders.customer_id = Customers.customer_id”
“customer_name”
“C4 has no matching customer.”
“C3 has no matching order.”
Render the tables and values exactly as given. Add no other text.

ACCURACY:
INNER has exactly 101/Mina and 102/Ravi. LEFT also has 103/C4 with missing
customer columns. FULL OUTER also has the Jo row with missing order columns.
Use NULL as a missing-value marker, not as ordinary text data. Query order
defines the left and right tables. FULL OUTER support varies by SQL dialect.
Do not invent data or metrics. No logo or watermark.
```
