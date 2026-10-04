# SQL JOIN: matching rows across two tables

**Audience:** A-level, university, and early-career software learners.  
**Complexity:** Intermediate.  
**Status:** sourced visual content draft.

## Learning objective

Predict which rows appear when two tables are joined on a key, and explain how `INNER JOIN`, `LEFT JOIN`, and `FULL OUTER JOIN` treat unmatched rows.

## Main claim

A join pairs rows when its `ON` condition matches; the join type determines which unmatched rows remain in the result.

## Worked example

**Orders**

| order_id | customer_id |
|---:|---|
| 101 | C1 |
| 102 | C2 |
| 103 | C4 |

**Customers**

| customer_id | customer_name |
|---|---|
| C1 | Mina |
| C2 | Ravi |
| C3 | Jo |

Join condition: `Orders.customer_id = Customers.customer_id`.

- **INNER JOIN:** matched pairs only → `(101, Mina)`, `(102, Ravi)`.
- **LEFT JOIN:** all rows from `Orders` plus matches → also `(103, NULL)` because `C4` has no customer row.
- **FULL OUTER JOIN:** all matched pairs plus unmatched rows from both sides → also `(103, NULL)` and `(NULL, Jo)`.

For a `LEFT JOIN`, nulls in the right-side columns mark the absence of a matching row; they are not the text string `"NULL"`.

## Supporting details

- A join is based on a condition, commonly equality between keys. It is not limited to matching columns with identical names.
- If a join key appears more than once on both sides, each qualifying pair can produce an output row. Duplicates can therefore multiply rows.
- The left and right sides are determined by query order. Reversing table order changes which side a `LEFT JOIN` preserves.
- SQL dialect support and syntax can vary. Use PostgreSQL behavior as the concrete reference for this sample; note that `FULL OUTER JOIN` support differs across database systems.

## Misconceptions and boundaries

- `INNER JOIN` does not preserve unmatched rows.
- `LEFT JOIN` keeps all left-side rows, not all rows from both tables.
- `NULL` in an outer-join result means no matching right-side value was available for that output row; it is not a default data value.
- A join condition with duplicate keys can produce more rows than either input table.

## Exact learner-facing copy

- `JOIN rows when ON is true.`
- `INNER: matched pairs only`
- `LEFT: every left row + matches`
- `FULL OUTER: every row from both sides`
- `No match? Missing-side columns become NULL.`
- `Duplicate keys can multiply result rows.`
- `Orders.customer_id = Customers.customer_id`
- `C4 has no matching customer.`
- `C3 has no matching order.`

## Sources

- [PostgreSQL 16: Joins Between Tables](https://www.postgresql.org/docs/16/tutorial-join.html) — join conditions, inner joins, left joins, unmatched-row behavior, and null-filled output columns.
- [PostgreSQL 16: Table Expressions](https://www.postgresql.org/docs/16/queries-table-expressions.html) — joined table expressions and outer-join semantics.
