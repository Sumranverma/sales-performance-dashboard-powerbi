# Power BI Build Guide

## 1. Load the Data

Open Microsoft Power BI Desktop.

Select:

Home → Get Data → Text/CSV

Import:

- data/sales_data.csv
- data/date_dimension.csv

Rename the tables:

- sales_data → Sales
- date_dimension → Date

## 2. Set Data Types

In the Sales table:

- Order_ID → Text
- Order_Date → Date
- Region → Text
- Category → Text
- Product → Text
- Customer_Segment → Text
- Salesperson → Text
- Quantity → Whole Number
- Unit_Price → Decimal Number
- Discount → Decimal Number
- Sales → Decimal Number
- Cost → Decimal Number
- Profit → Decimal Number

## 3. Create the Relationship

Go to Model view.

Create this relationship:

Date[Date] → Sales[Order_Date]

Relationship:

One-to-many

The Date table should be on the "one" side.

## 4. Create Measures

Create the DAX measures provided in:

docs/dax_measures.txt

## 5. Dashboard Pages

Create four report pages:

### Executive Overview

Include:

- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Profit Margin %
- Average Order Value
- Monthly Sales Trend
- Sales by Region
- Sales by Category

### Product Performance

Include:

- Sales by Product
- Profit by Product
- Quantity by Product
- Sales by Category
- Top 10 Products

### Regional Analysis

Include:

- Sales by Region
- Profit by Region
- Orders by Region
- Monthly Regional Sales Trend

### Detailed Analysis

Create a detailed table containing:

- Order_ID
- Order_Date
- Region
- Category
- Product
- Customer_Segment
- Salesperson
- Quantity
- Sales
- Cost
- Profit

## 6. Slicers

Add slicers for:

- Date
- Region
- Category
- Customer Segment
- Salesperson

## 7. Final Checks

Test:

- Slicers
- Cross-filtering
- Drill-down
- Date filtering
- Product filtering
- Regional filtering

Save the completed Power BI report as:

Sales_Performance_Dashboard.pbix
