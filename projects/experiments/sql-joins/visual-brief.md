# Visual brief: SQL joins

Use the shared visual style in `docs/STYLE.md`. This sample has more relational detail than the stack example.

## Visual thesis

The join condition determines the matching pairs; the join type determines which unmatched rows survive.

## Composition

- Portrait 4:5 page; retain the shared paper, typography, linework, semantic colors, and restrained technical texture.
- Use two compact, legible source tables around one dominant “rows meet on the key” relationship diagram.
- Highlight matching `customer_id` values in teal and matched result rows in copper.
- Show three result panels of different visual weight: INNER (matched rows), LEFT (all Orders plus a NULL-filled unmatched order), FULL OUTER (also the unmatched customer Jo).
- Connect the table rows to the output rows with fine leader lines; make the C4 and C3 unmatched cases easy to trace.
- Add a small duplicate-key inset showing that repeated keys can produce multiple qualifying pairs.
- Use a compact side note for the syntax: `Orders.customer_id = Customers.customer_id`.
- Avoid relying on Venn diagrams alone; the exact row output is the lesson.

## Required checks

- Source tables must contain Orders 101/C1, 102/C2, 103/C4 and Customers C1/Mina, C2/Ravi, C3/Jo.
- INNER output is exactly 101/Mina and 102/Ravi.
- LEFT output also includes 103 with NULL customer fields.
- FULL OUTER output also includes Jo with NULL order fields.
- Preserve input order when naming left versus right; explain that FULL OUTER support varies by SQL dialect.
