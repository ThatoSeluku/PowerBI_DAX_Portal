# AVERAGEX DAX Examples

The `AVERAGEX` function is used to calculate the average of an expression evaluated over a table. Below are three common examples of how `AVERAGEX` can be applied in DAX calculations.

---

## 1. Average Sales Price Per Product

**Scenario**: Calculate the average sales price per product.

```DAX
Average Sales Price = AVERAGEX(SalesTable, SalesTable[TotalSales] / SalesTable[Quantity])
```

## 2. Average Profit Margin

**Scenario**: Calculate the average profit margin per product
```DAX
Average Profit Margin = AVERAGEX(Products, (Products[Sales] - Products[Cost]) / Products[Sales])
```

## 3. Average Discount Applied

**Scenario**: Calculate the average discount applied
```DAX
Average Discount = AVERAGEX(SalesTable, SalesTable[DiscountAmount] / SalesTable[OriginalPrice])
```
