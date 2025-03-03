# SUMX DAX Examples

The `SUMX` function is used to evaluate an expression for each row in a table and then sum the results. Below are three common examples of how `SUMX` is applied in DAX calculations.

---

## 1. Total Revenue Calculation

**Scenario**: Calculate total revenue by multiplying the quantity and price for each row and summing the results.

```DAX
Total Revenue = SUMX(SalesTable, SalesTable[Quantity] * SalesTable[Price])

