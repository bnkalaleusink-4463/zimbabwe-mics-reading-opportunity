# Variable Notes

This document records the focal variables used in the cleaned GitHub analysis.

| Variable | Working interpretation | Valid coding used in analysis |
|---|---|---|
| `PR3` | Number of children's or picture books | 0–10 retained; 10 represents 10+; special/structural missing excluded |
| `FL6A` | Child reads books | 1 = Yes, 2 = No; special/structural missing excluded |
| `FL6B` | Someone reads books to child | 1 = Yes, 2 = No; special/structural missing excluded |
| `FL10` | Child likes reading stories | 1 = Yes, 2 = No; special/structural missing excluded |

## Derived variables

### `child_books_n`

Created from `PR3` using only valid values 0–10. Special code `99` and structural missing values are excluded.

### `has_child_book`

Created only for observations with valid `child_books_n`:

- `0` = no children's/picture books
- `1` = at least one children's/picture book

Missing values remain missing and are not recoded as `0`.

## Interpretation discipline

`FL10` is treated specifically as reported/indicated **liking reading stories**. It should not be expanded into a general measure of reading motivation.

The focal variables have different valid denominators. Aggregate percentages therefore cannot establish an individual-level mismatch between liking stories and having access to books or reading support.

All current results are unweighted sample descriptives, not national prevalence estimates.
