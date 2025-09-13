# Data-Analytics-Market Analysis Project 
# Market Analysis & Business Insights

## Project Overview
This project analyzes sales and customer data to uncover key business insights. The goal is to identify high-value customers, underperforming products, and regional revenue contributions to guide strategic decision-making.

## Tools & Technologies
- SQL (SQLite) for data querying
- Google Sheets / Excel for dashboards and visualization

## Dataset
- Dataset contains sales transactions including:
  - Order ID
  - Product Name & Category
  - Sales Amount
  - Profit
  - Quantity
  - Region
  - Customer Segment
  - Payment Method
  - Marketing Channel
  - Date
- Sample dataset: `sample_data.csv`

## Key Analyses
1. **Customer Segmentation**
   - Segmented customers into high-value, mid-value, and low-value to identify priority targets.

2. **Regional Revenue Contribution**
   - Revenue contribution by region: West, East, South, North.

3. **Sales by Payment Method**
   - Insights on customer payment preferences.

4. **Sales by Marketing Channel**
   - Determines which marketing channels drive the most sales.

5. **Sales vs Profit by Sub-Category**
   - Highlights sub-categories with the highest profitability.

6. **Top Products & Categories**
   - Identifies best-selling products and categories.

7. **Trend Analysis**
   - Monthly or seasonal sales trends to guide forecasting and inventory planning.

## Sample Queries
```sql
-- Sales by Payment Method
SELECT Payment_Method, ROUND(SUM("Sales Amount"),2) AS total_sales
FROM sales_data
GROUP BY Payment_Method
ORDER BY total_sales DESC;

-- Regional Revenue Contribution
SELECT Region, ROUND(SUM("Sales Amount"),2) AS total_sales
FROM sales_data
GROUP BY Region
ORDER BY total_sales DESC;

