# ALL Function in DAX

The `ALL` function in DAX is used to remove filters from a table or column. It can be helpful when you want to calculate a measure without considering certain filters in the data model, or when you need to compare a subset of data to the overall dataset.

---

## 1. **Basic Usage of ALL**

The simplest use of `ALL` is to remove filters on a specific column or table.

**Example**: Calculating the total sales without any filters.

```DAX
Total Sales (All) = CALCULATE(SUM(Sales[Amount]), ALL(Sales))
```

## 2. Using ALL on a Specific Column
You can use ALL on a specific column to remove filters only from that column.

**Example:** Calculating total sales without any filter on the Product[Category] column.

```DAX
Total Sales (All Categories) = CALCULATE(SUM(Sales[Amount]), ALL(Product[Category]))
```
**Here:**
ALL(Product[Category]) removes any filters that may have been applied to the Product[Category] column, and the calculation is done over all categories.

## 3. Using ALL with Multiple Columns
ALL can also be used with multiple columns to remove filters from a combination of columns.

**Example:** Calculating the total sales without filters on both Product[Category] and Sales[Region].

```DAX
Total Sales (All Categories and Regions) = CALCULATE(
    SUM(Sales[Amount]),
    ALL(Product[Category], Sales[Region])
)
```
**Here:**
ALL(Product[Category], Sales[Region]) removes filters on both the Product[Category] and Sales[Region] columns, and the total sales is calculated across all categories and regions.
