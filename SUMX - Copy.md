# AVERAGEX DAX Examples

The `AVERAGEX` function is used to calculate the average of an expression evaluated over a table. Below are three common examples of how `AVERAGEX` can be applied in DAX calculations.

---

## 1. Average Sales Price Per Product

**Scenario**: Calculate the average sales price per product.

```DAX
Average Sales Price = AVERAGEX(SalesTable, SalesTable[TotalSales] / SalesTable[Quantity])
```

