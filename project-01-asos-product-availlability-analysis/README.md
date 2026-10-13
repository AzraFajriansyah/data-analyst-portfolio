# ASOS Product Availability & Revenue Opportunity Analysis

## Overview

This project examines how product availability affects potential revenue opportunities across ASOS's product catalog. Using Python, I cleaned and analyzed product pricing and size availability data, extracted brand names from product descriptions where necessary, and assessed stockout levels across individual products and brands.

The objective is to identify potential revenue exposure associated with unavailable sizes and highlight brands where stock availability issues may have the greatest financial impact. Rather than estimating actual lost sales, the analysis provides a directional assessment of potential revenue opportunities based on product prices and stock availability.

The analysis covers the following steps:

- Loading the product catalog into a pandas DataFrame.
- Cleaning and standardizing price values and removing invalid records.
- Extracting brand names from product descriptions when a standardized brand column is unavailable.
- Calculating stockout counts and rates from product size availability data.
- Aggregating results by brand to compare average prices, stockout rates, and estimated revenue exposure.
- Visualizing the relationship between product prices and stockout rates to identify brands with notable availability risks.

## Dataset

The dataset is located at `data/products_asos.csv`. It contains product-level information, including product names, categories, size availability, colors, prices, and descriptions. The description field is also used to infer brand names when a standardized brand column is not available.

## Methodology

The `size` field serves as the primary indicator of product availability. Since each product may contain multiple size entries in a single string, entries labeled `"Out of stock"` are counted as unavailable sizes.

The notebook calculates the following metrics:

- `Stockout_Count`: The number of unavailable sizes listed for a product.
- `Stockout_Rate`: The proportion of unavailable sizes relative to the total number of listed sizes.
- `Lost_Revenue`: An estimated revenue exposure calculated by multiplying the product price by its stockout count.

These metrics provide a simplified view of product availability and its potential financial implications. The estimated revenue exposure is intended to support comparisons across products and brands, rather than serve as a direct measure of actual lost sales.

## Key Findings

- **ASOS has the largest estimated revenue exposure.** Its extensive product catalog contributes to the highest overall exposure in absolute terms.
- **New Look shows a relatively high stockout rate.** Compared with many larger brands, its availability patterns indicate a potential area of concern.
- **Higher-priced products with elevated stockout rates warrant closer attention.** These products may represent greater potential revenue opportunities if availability improves.
- **Brand-level comparisons can help prioritize inventory improvements.** The analysis highlights where availability issues may have the greatest potential financial impact.

## Repository Structure

```text
.
├── data/
│   └── products_asos.csv
├── notebooks/
│   └── asos_product_availability_analysis.ipynb
└── README.md
```

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Limitations

The estimated revenue exposure is based on product prices and the number of unavailable sizes. It does not account for actual customer demand, purchasing behavior, or the likelihood of a sale.

Therefore, the estimates should not be interpreted as actual lost revenue. Instead, they provide a directional indicator of potential revenue opportunities and help identify brands that may warrant further investigation into product availability.
