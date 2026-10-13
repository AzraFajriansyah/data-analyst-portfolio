# Cafe Sales Performance Dashboard

## Overview

This project focuses on analyzing sales performance across six cafe branches in Indonesia using Microsoft Excel. Starting with raw transaction data, I consolidated sales records, enriched them with product information, and developed an interactive dashboard to provide a clear overview of business performance.

The dashboard helps identify top-performing branches, best-selling products, revenue contributions by category, and daily sales trends. Its primary objective is to transform raw transaction data into actionable insights that support business monitoring and decision-making.

## Data and Workbook Structure

The main workbook is located at `dashboard/cafe_sales_performance_dashboard.xlsx`.

The workbook is organized into the following sheets:

- **Branch sheets:** Contain raw transaction records for each of the six locations.
- **`DBProduct`:** Stores product reference data, including `ProdukID`, `Produk`, and `Kategori`.
- **`Master`:** Contains the consolidated sales dataset, enriched with product names, date fields, and category information.
- **`Dashboard` and `Detail1`:** Present summarized sales metrics, visualizations, and supporting details.

The consolidated dataset includes the following fields:

- Transaction date
- Branch
- Product ID
- Quantity
- Unit price
- Total sales
- Product name
- Product category

The analysis covers six branches located in Makassar, Semarang, Medan, Bandung, Surabaya, and Jakarta.

## Dashboard Features

The dashboard is designed to provide an overview of key sales performance indicators, including:

- **Branch performance:** Compare total sales across locations to identify the strongest-performing branches.
- **Product performance:** Identify products that contribute the most to total revenue.
- **Category contribution:** Evaluate how individual product categories contribute to overall sales.
- **Daily sales trends:** Monitor sales fluctuations and identify dates with unusually high sales activity.

By consolidating these metrics into a single Excel dashboard, the project makes sales performance easier to monitor without requiring a separate business intelligence platform.

## Key Findings

The analysis shows approximately IDR 50.5 million in total sales across the six branches. Several notable patterns emerge from the workbook:

- **Coffee is the leading category**, contributing the largest share of total revenue.
- **Bandung, Semarang, and Surabaya** are among the strongest-performing branches based on total sales.
- **Mocha and Americano** are the leading products by revenue.
- **Several dates in late September** recorded some of the highest daily sales totals, indicating periods of increased sales activity.

These findings provide a starting point for evaluating branch performance, reviewing product priorities, and investigating changes in daily sales patterns.

## Repository Structure

```text
.
├── dashboard/
│   └── cafe_sales_performance_dashboard.xlsx
└── README.md
```

## Tools & Technologies

- Microsoft Excel
- PivotTables
- Charts and data visualization
- Data cleaning and transformation
- Dashboard design

## Limitations

The analysis is based on the transaction records available in the workbook. Although the dashboard highlights sales patterns and differences in branch performance, it does not establish the underlying causes of those patterns.

For example, higher sales during late September cannot be directly attributed to seasonal demand or promotional activities without additional information. Similarly, total sales alone do not indicate profitability, as costs, margins, and operating expenses are not included in the analysis.

The findings should therefore be interpreted as descriptive sales insights rather than definitive explanations of business performance.
