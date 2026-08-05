# Coffee-Shop-Analysis
## Sales_Analysis_Project

### Project Overview

This project aims to analyse the sales of a coffee shop to uncover business insights related to sales performance, customer purchasing patterns, product performance, and time-based trends.and hence provide recommendations for maximising sales and revenue.

### Data Sources

Sales Data: The dataset used in this analysis is the "Coffee Shop Sales.csv" file, containing detailed information about each sale made by the company.

### Tools

- Excel - Data Cleaning
- Snowflake - Data Analysis
  
### Data Preparation
In the initial data cleaning phase, we performed the following tasks:
1. Data loading and inspection
2. Handling missing values
3. Checking duplicates
4. Data cleaning and formatting

### Feature Engineering
Created new analytical features
Added the Sales Column

```SQL
ALTER TABLE T1
ADD COLUMN sales NUMBER(10,2);
```

```SQL
UPDATE T1
SET Sales = transaction_qty * unit_price;
```

This step transformed the raw transactional data into a format suitable for revenue analysis.

### Exploratory Data Analysis
-

### Data Analysis

#### KPIs Calculated:
- Total Sales
- Total Quantity Sold
- Total Transactions

#### Product Performance Analysis
- Best-selling categories
- Best-selling product types
- Best-selling products
- 
#### Time-based Analysis
I created custom time groups using a CASE statement.

#### Time Groups
|Time-Range  |Group|
|06:00-09:00 |Morning|



### Results/Findings

#### Sales Trends
- Revenue increased month-over-month.
- June generated the highest sales.

#### Customer Behavior
- Early Day was the busiest trading period.
- Evening generated the lowest sales among standard operating hours.
  
#### Product Performance
- Certain product categories contributed significantly more revenue than others.
- Product-level analysis highlighted the top-selling items.

### Recommendations

- Schedule more baristas and cashiers during the Early Day period.
- Ensure sufficient inventory is available before this peak period.
- Reduce staffing during quieter periods where appropriate.
- Run promotions during slower periods.
- Focus marketing on top-performing months: Investigate what drove higher sales in June and replicate successful      promotions or seasonal campaigns.
- Expand high-performing product categories.
- Review low-performing products.
- Improve inventory planning, that is, increase stock before busy months, order fewer slow-moving products and
reduce stock shortages during peak periods.

  
### Limitations

### References


