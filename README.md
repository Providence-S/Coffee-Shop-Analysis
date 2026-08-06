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
These were the key business questions:
1. What is the overall sales trend?
2. What products are top/bottom sellers?
3. What are the peak sales periods?
4. Which months had the most/least sales?
5. Best/worst performing store location?

### Data Analysis

#### KPIs Calculated:
- Total Sales
- Total Quantity Sold
- Total Transactions

#### Product Performance Analysis
- Best-selling categories
- Best-selling product types
- Best-selling products
  
#### Time-based Analysis
I created custom time groups using a CASE statement.

#### Time Groups
|Time-Range  |Group    |
|------------|---------|
|06:00-09:00 |Morning  |
|09:01-12:00 |Early Day|
|12:01-15:00 |Mid Day  |
|15:01-18:00 |Late Day |
|18:01-21:00 |Evening  |

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

While this project provides valuable insights into coffee shop sales performance, a few limitations should be considered.
1. The dataset covers only January to June, meaning seasonal trends for the full year cannot be evaluated.
   - The impact of this is that annual sales patterns cannot be determined and holiday and festive season effects are not captured.
2. No Customer information.
   - The dataset does not include customer-related attributes such as customer ID, age, gender, purchase history and hence customer segmentation cannot be performed.
3. The dataset does not include ost of goods sold, operating expenses and profit margins.
   - Therefore, profitability could not be measured and high selling products may not necessarily be the most profitable.

### Business Value

This analysis demonstrates how SQL can be used not only to retrieve data but also to uncover actionable insights that support operational efficiency, inventory management, staffing decisions, marketing strategies, and revenue growth.

### 📚 Key Learnings

Through this project, I strengthened my understanding of:
- Writing SQL queries in Snowflake
- Exploratory Data Analysis (EDA)
- Data quality assessment
- Feature engineering using SQL
- Aggregate functions and grouping
- Temporary tables
- CASE statements for business logic
- Time-based sales analysis
- Translating data into actionable business insights

This project also reinforced the importance of validating data before analysis and demonstrated how SQL can be used to solve real business problems.

### References
