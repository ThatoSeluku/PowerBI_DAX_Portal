# Year-to-Date (YTD) DAX Examples

Time intelligence functions in DAX help analyze data across different periods. The `TOTALYTD` function is commonly used for calculating Year-to-Date (YTD) values. Below are three practical examples of `YTD` calculations.

---

## 1. Total Sales Year-to-Date

**Scenario**: Calculate the total sales from the beginning of the year to the current date.

```DAX
Total Sales YTD = TOTALYTD(
    SUM(Sales[SalesAmount]),
    Sales[Date]
)
```


## 2. Cumulative Profit Year-to-Date

**Scenario**: Calculate the total profit from beginning of the year till now
```DAX
Cumulative Profit YTD = TOTALYTD(
    SUM(Sales[Profit]),
    Sales[Date]
)
```

## 3.Year-to-Date Customer Count

**Scenario**: Calculate the total number of customers from the beginning of the year
```DAX
YTD Customer Count = TOTALYTD(
    DistinctCount(Sales[Customer]),
    Sales[Date]
)
```

Note: DistinctCount helps count the unique number of customers we have here. A normal count would've included all values.



# Month-to-Date (MTD) DAX Examples

MTD (Month-to-Date) calculations are used to aggregate data from the start of the current month up to the current date. This is similar to YTD, but focused on the month. Below are three common MTD DAX examples.

---

## 1. Total Sales Month-to-Date

**Scenario**: Calculate the total sales from the beginning of the current month to the current date.

```DAX
Total Sales MTD = TOTALMTD(
    SUM(Sales[SalesAmount]),
    Sales[Date]
)
```



## 2. Cumulative Profit Month-to-Date

**Scenario**: Calculate the total profit from beginning of the month till now
```DAX
Cumulative Profit MTD = TOTALMTD(
    SUM(Sales[Profit]),
    Sales[Date]
)
```

## 3.Month-to-Date Customer Count

**Scenario**: Calculate the total number of customers from the beginning of the month
```DAX
YTD Customer Count = TOTALYTD(
    DistinctCount(Sales[Customer]),
    Sales[Date]
)
```

