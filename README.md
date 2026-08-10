# Retail Sales & Growth Analysis Dashboard

## Project Overview
A Power BI-based retail sales analysis project using the supplied `sales_data.csv` dataset.

The project focuses on analyzing sales and profit performance by date, region, and product.

## Tools
- Power BI
- Power Query
- DAX
- SQL
- CSV

## Dataset
The supplied dataset contains 6 records and the following fields:

- `OrderID`
- `Date`
- `Region`
- `Product`
- `Sales`
- `Profit`

> Note: This sample dataset is small. The project is presented as a portfolio/learning project and does not claim large-scale production analysis.

## Analysis Areas
- Total Sales
- Total Profit
- Sales by Region
- Profit by Region
- Sales by Product
- Profit by Product
- Sales trend over time
- Profit margin analysis

## Suggested KPI Measures

### Total Sales
```DAX
Total Sales = SUM(sales_data[Sales])
```

### Total Profit
```DAX
Total Profit = SUM(sales_data[Profit])
```

### Profit Margin
```DAX
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
```

### Order Count
```DAX
Order Count = DISTINCTCOUNT(sales_data[OrderID])
```

## Recommended Dashboard Layout

### Page 1 — Executive Dashboard
- KPI cards: Total Sales, Total Profit, Profit Margin, Order Count
- Sales by Region
- Profit by Region
- Sales by Product
- Sales Trend by Date
- Region and Product slicers

### Page 2 — Detailed Analysis
- Region-level table
- Product-level table
- Profit margin comparison
- Date-level sales/profit trend

### Page 3 — Insights & Recommendations
Use only findings supported by the actual data. Avoid inventing business conclusions.

## Data Preparation
Recommended Power Query checks:
- Set `Date` to Date type.
- Set `Sales` and `Profit` to numeric types.
- Check duplicate `OrderID` values.
- Check missing values.
- Validate that sales/profit values are reasonable.
- Create a proper Date table if the analysis is expanded to a larger time-series dataset.

## SQL
See [`sql_analysis.sql`](sql_analysis.sql) for equivalent analysis queries.

## Power BI File
Place the final `.pbix` file in the `powerbi/` folder.

## Dashboard Screenshot
Place a screenshot of the final dashboard in the `screenshots/` folder and add it below:
## Dashboard Preview

![Retail Sales Dashboard](./screenshots/dashboard.png)

## Interview Explanation
A concise explanation:

> "I built a Retail Sales & Growth Analysis dashboard in Power BI to analyze sales and profitability across products, regions, and dates. I prepared the data using Power Query, created DAX measures for key KPIs such as total sales, total profit, profit margin, and order count, and used interactive visuals to identify performance patterns. I also prepared SQL queries to reproduce the core analysis."

## Important
The supplied sample contains only 6 rows, so the project should be discussed honestly as a portfolio/learning project. If a larger dataset is later used, update the README and analysis accordingly.
