# Sales Performance Dashboard - Power BI & Tableau

## Project Overview
This project involves building an **interactive sales performance dashboard** using **Power BI & Tableau**. The dashboard provides insights into sales trends, revenue, and regional performance using real-world datasets.

## Features
- **Sales Trend Analysis:** Identify revenue trends over time.
- **Regional Performance:** Compare sales across different regions.
- **Product Category Insights:** Analyze which products generate the most revenue.
- **Profitability Metrics:** Track profit margins and cost efficiency.
- **Dynamic Filtering:** Allow users to drill down into key performance indicators.

## Dataset
The dataset consists of sales transaction records with the following fields:
- **Order Date**: The date of transaction
- **Customer ID**: Unique identifier for customers
- **Product Category**: Classification of sold products
- **Sales Amount**: Total sales value
- **Profit Margin**: Profitability per transaction
- **Region**: Location of sales transaction

## Steps to Build the Dashboard
### 1. Data Extraction (SQL Query)
Extract data from a database using the following query:
```sql
SELECT OrderDate, CustomerID, ProductCategory, SalesAmount, ProfitMargin, Region 
FROM SalesTransactions 
WHERE OrderDate BETWEEN '2023-01-01' AND '2023-12-31';
```
### 2. Data Preprocessing (Python)
Prepare data for visualization using Python:
```python
import pandas as pd

# Load dataset
df = pd.read_csv("sales_data.csv")

# Convert date column to datetime format
df['OrderDate'] = pd.to_datetime(df['OrderDate'])

# Remove missing values
df = df.dropna()

# Save cleaned data
df.to_csv("cleaned_sales_data.csv", index=False)
print("Data cleaning completed!")
```
### 3. Data Visualization
- **Power BI:** Create interactive reports with filters and drill-through capabilities.
- **Tableau:** Build dashboards for advanced data storytelling and insights.

## Files & Resources
- `sales_data.csv` - Sample dataset
- `cleaned_sales_data.csv` - Preprocessed data
- `dashboard.pbix` - Power BI dashboard file
- `dashboard.twbx` - Tableau workbook
- `README.md` - Project documentation

## Insights & Takeaways
- **Top-Performing Regions:** Identify locations driving revenue growth.
- **Best-Selling Products:** Analyze which categories generate the highest sales.
- **Seasonal Trends:** Understand how sales fluctuate throughout the year.

## How to Use
1. Clone this repository.
2. Load `cleaned_sales_data.csv` into Power BI or Tableau.
3. Open `dashboard.pbix` or `dashboard.twbx` to explore insights.

## Repository Link
🔗 [GitHub Repository](https://github.com/your-repository-link)
