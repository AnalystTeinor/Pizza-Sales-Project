# Pizza-Sales-Analysis

## Project Overview

The Pizza Sales Project is an all-inclusive system made to monitor and evaluate pizza sales data, offering insightful information to improve decision-making and business operations.  The goals of this project are to increase sales performance, streamline inventory control, and use data-driven analysis to determine client preferences.

### Data Sources

Sales Data: The primary dataset used for this analysis is the 'pizza_sales_data.csv' file, containing detailed information about each sale made by the company. 

### Tools

- Excel - Data Cleaning & Creating reports
- SQL Server - Data Analysis

### Data Cleaning/Preparation

1. Data loading and inspection.
2. Data cleaning and formation.

### Exploratory Data Analysis

- What is the overall revenue generated
- What is the average pizza sold per order
- Total Pizza sold by Pizza category

### Data Analysis

Some codes used 

```sql

Select  pizza_name, sum(quantity) as Rank_of_pizza
from pizza_sales_dup
group by pizza_name
order by Rank_of_pizza asc;


select
hour(order_time) As order_hours,
count(distinct order_id) as Total_orders
from pizza_sales_dup
group by order_hours
order by total_orders;


Select pizza_category, Round(sum(total_price) *100 /
 (Select sum(total_price)from pizza_sales_dup),2) as PCG_sales_pizza_category
from pizza_sales_dup
group by pizza_category;

```

### Results/Findings

1. Peak Sales Periods: The highest sales occur during (12:00:00 - 13:00:00) and on Friday and Saturdays, highlighting key revenue-generating timeframes.
2. Best-Selling Products: Certain pizza varieties, such as The Classic Deluxe Pizza and The Barbecue Chicken Pizza, consistently generate the highest revenue.
3. Pizza Size Preferences: Large pizzas account for the majority of sales, followed by Medium pizzas, with XX-Large pizzas having lower sales volume.

### Recommendations 

The following suggestions can improve customer satisfaction, boost profitability, and optimize business performance based on the results of the pizza sales analysis:

-  Introduce special promotions during holidays, sporting events, and weekends to capitalize on increased demand.
-  Improve the user experience on digital ordering platforms, ensuring seamless navigation, payment options, and order tracking.
-  Introduce a customer loyalty program that incentivizes repeat purchases through discounts, free items, or points-based rewards.
-  Provide more flexibility in pizza customization to cater to diverse customer preferences, including dietary restrictions.

### 
