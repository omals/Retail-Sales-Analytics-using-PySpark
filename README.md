# Retail Sales Analytics using PySpark

## Project Overview

This project performs an end-to-end Retail Sales Analysis using **PySpark** and **Spark SQL** on the Superstore dataset. The objective is to analyze sales performance, profitability, customer behavior, product performance, and regional trends to provide actionable business recommendations.

## Business Problem

Management requires answers to the following questions:

### Sales Performance
- Which regions generate the highest sales?
- Which categories contribute the most revenue?
- How are sales trending over time?

### Profitability
- Which categories and products generate the most profit?
- Which products are causing losses?

### Customer Analytics
- Who are the most valuable customers?
- Which customers should be targeted for loyalty programs?

### Product Analytics
- Which products perform best?
- Which products should be promoted?

### Business Strategy
- Where should the company invest more?
- Which areas need improvement?

---

## Technologies Used

- PySpark
- Spark SQL
- Databricks
- Python
- Jupyter Notebook

---

## Dataset

Dataset Source:

https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

The dataset contains:

- Orders
- Customers
- Products
- Categories
- Regions
- Sales
- Profit
- Discounts
- Shipping Information

---

# Data Validation

Before performing analysis, the dataset was validated to ensure data quality and consistency.

## Validation Checks Performed

### Row and Column Validation
- Verified total number of rows.
- Verified total number of columns.

### Schema Validation
- Inspected schema and column names.
- Validated data types.

### Null Value Validation
Checked for missing values in:

- Customer ID
- Customer Name
- Product Name
- Sales
- Profit
- Order Date
- Ship Date

### Duplicate Record Validation
Validated duplicate records using:

- Complete row comparison
- Order-level verification

### Date Validation
Validated:

- Order Date
- Ship Date

Checks included:

- Invalid dates
- Missing dates
- Future dates

### Data Type Validation
Verified correct data types for:

| Column | Type |
|----------|----------|
| Sales | Numeric |
| Profit | Numeric |
| Quantity | Numeric |
| Discount | Numeric |
| Order Date | Date |
| Ship Date | Date |

---

# Data Preparation

The following transformations were performed.

## Date Conversion

Converted:

- Order Date
- Ship Date

into proper date format.

## Derived Columns

### Order Year
Extracted year from Order Date.

### Order Month
Extracted month from Order Date.

### Profit Category

| Profit Range | Category |
|-------------|----------|
| Profit < 0 | Loss |
| 0 - 500 | Low Profit |
| 500 - 2000 | Medium Profit |
| > 2000 | High Profit |

### Sales Category

| Sales Range | Category |
|-------------|----------|
| Sales < 100 | Low |
| 100 - 500 | Medium |
| > 500 | High |

---

# KPI Analysis

## Sales KPIs

- Total Sales
- Total Orders
- Average Order Value

## Profit KPIs

- Total Profit
- Average Profit per Order

## Customer KPIs

- Total Customers

---

# Regional Analysis

Performed:

- Sales by Region
- Profit by Region
- Average Order Value by Region

### Outcomes

- Best Performing Region
- Worst Performing Region
- Regional Revenue Contribution
- Regional Profitability Comparison

---

# Category Analysis

Analyzed:

- Sales by Category
- Profit by Category
- Sales by Sub-Category
- Profit by Sub-Category

### Outcomes

- Most Profitable Category
- Least Profitable Category
- Best Selling Sub-Category
- Lowest Performing Sub-Category

---

# Customer Analysis

## Top Customers by Sales

Identified top 10 customers based on sales contribution.

## Top Customers by Profit

Identified top 10 customers based on profit contribution.

## Customer Segmentation

- Consumer
- Corporate
- Home Office

## VIP Customers

Defined as:

> Top 10 customers based on total sales.

---

# Product Analysis

## Top Products

- Top 10 Products by Sales
- Top 10 Products by Profit

## Bottom Products

- Bottom 10 Products by Profit

## Loss Making Products

Identified products generating negative profit.

---

# Trend Analysis

## Monthly Sales Trend

Analyzed monthly revenue performance.

## Monthly Profit Trend

Analyzed monthly profitability performance.

## Best Sales Month

Identified month with highest sales.

## Worst Sales Month

Identified month with lowest sales.

---

# Window Function Analysis

Implemented advanced analytics using PySpark Window Functions.

## Product Ranking

Ranked products within each category based on sales.

## Customer Ranking

Ranked customers within each region based on sales.

## Top Product per Category

Identified highest-selling product within each category.

## Top Customer per Region

Identified highest-spending customer within each region.

## Running Sales

Calculated cumulative monthly sales.

## Month-over-Month Growth

Calculated:

- Previous Month Sales using `lag()`
- MoM Growth Percentage

---

# Spark SQL Analysis

Created temporary views and performed SQL analysis.

### SQL Queries Implemented

- Sales by Region
- Profit by Category
- Top 10 Customers
- Monthly Sales Trend

---

# Business Insights

1. The highest-performing region contributes the largest share of revenue.
2. The lowest-performing region requires targeted growth initiatives.
3. Technology products generate the highest profitability.
4. Furniture generates strong revenue but lower profit margins.
5. A small group of customers contributes a significant share of total sales.
6. VIP customers should be retained through loyalty programs.
7. Certain products consistently generate losses.
8. Seasonal trends influence sales performance.
9. Some sub-categories have high sales but low profitability.
10. Top-performing products should receive additional marketing support.

---

# Recommendations

## 1. Invest in High-Performing Regions
Increase marketing spend and inventory allocation.

## 2. Promote High-Profit Categories
Focus campaigns on categories generating the highest profit.

## 3. Review Discount Strategy
Reduce excessive discounts impacting profitability.

## 4. Retain VIP Customers
Launch customer loyalty and reward programs.

## 5. Improve Underperforming Regions
Introduce region-specific marketing strategies.

## 6. Reprice or Remove Loss-Making Products
Evaluate pricing and profitability.

## 7. Optimize Inventory Planning
Use trend analysis to improve stock forecasting.

## 8. Cross-Sell Profitable Products
Increase revenue through strategic bundling.

---

# Project Structure

```text
Retail-Sales-Analytics-PySpark/
│
├── Business_Insights_Report.pdf
├── Project Summary.pdf
├── Retail_Sales_Analytics.ipynb
├── superstore.csv
└── README.md
```

---

# Conclusion

This project demonstrates how PySpark can be used for large-scale retail analytics by combining data validation, KPI analysis, trend analysis, customer segmentation, product analytics, Spark SQL, and business intelligence reporting to support data-driven decision-making.
