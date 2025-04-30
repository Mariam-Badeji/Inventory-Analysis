# INTRODUCTION
Effective inventory management is critical to operational efficiency, cost control, and customer satisfaction in any product-based business. This report presents a comprehensive analysis of an inventory dataset obtained from the FP20 Data Challenge (April edition), which simulates the inventory system of a hypothetical multinational company. The dataset includes 5,000 unique products spanning seven categories—Books, Clothing, Electronics, Home & Garden, Office Supplies, Sports, and Toys—alongside detailed information on stock levels, pricing, suppliers, restocking schedules, and geographic distribution across 10 European countries. The goal of this analysis is to uncover trends, identify inefficiencies, and provide actionable insights that can support smarter inventory planning, optimize stock movement, and minimize the risks of overstocking or stockouts.
# DATA DESCRIPTION
This dataset was obtained from the FP20 Data Challenge site for the (April edition). It represents a simulated inventory system for a hypothetical company, focusing on the management and logistics of various products. This dataset includes 5,000 unique product IDs, each linked to a specific product name. These products are categorized into seven distinct groups: Books, Clothing, Electronics, Home & Garden, Office Supplies, Sports, And Toys. Each item has an associated unit price (in USD). Inventory levels are tracked using the stock_quantity column, and each product is also assigned a qualitative stock level – low, mid, or high. A reorder point is defined for every product, representing the stock threshold at which a replenishment is automatically triggered. The ‘Lead_Time’ column indicates how long (in days) it takes for an item to arrive after ordering, while the ‘Last_Restock_Date’ records the most recent restocking date. 
There are 50 distinct product suppliers, each with a unique identifier and the inventory is distributed across 5,000 warehouse locations in 10 European countries: Austria, Belgium, France, Germany, Italy, Netherlands, Poland, Spain, Sweden, and the United Kingdom. Each ware is geotagged with its latitude and longitude. For restocking purposes, the dataset includes a minimum reorder quantity per product. The ‘Status’ column indicates whether a product is currently active or has been discontinued, and an ‘Entry_Date’ field specifies when each product was first added to the system. 
# METHODLOGY
The analysis of this dataset followed a structured workflow, consisting of the following key steps:
## 1.	Data Understanding
The dataset was first explored to understand the structure, column definitions, and the overall scope. Basic descriptive statistics Such as Average and standard deviation were used to get an overview of stock quantities, product categories, price distribution, and supplier distribution. 
## 2.	Date Preparation
The dataset required minimal cleaning. The data was generally well-structured and consistent, with no major issues such as missing values, duplicate entries, or formatting errors. Minor adjustments included:
•	Renaming a few column headers for clarity (e.g., Stock_Quantity → stock_quantity)
•	Converting date fields (e.g., Last_Restock_Date, Entry_Date) into datetime format
•	Ensuring numerical fields (e.g., Price, Lead_time) were in the correct data type for analysis
Overall, the dataset was analysis-ready upon initial inspection, which allowed the focus to remain on exploratory analysis and insights. 
## 3.	Exploratory Data Analysis (EDA)
Exploratory analysis was concluded to identify trends, outliers, and category-level patterns:
•	The distribution of stock quantities across categories
•	Identification of frequently understocked products (stock quantity < Reorder point)
•	Summary of products by Status (active – in stock vs discontinued – out of stock)
•	Analysis of average lead time (day) by suppliers
•	The monthly trend of restocking products
Visualizations such as bar charts, tree maps, pie charts, and line charts were used to support the analysis.
## 4.	Inventory Performance Metrics
Key inventory metrics were calculated to assess performance:
•	Inventory Turnover Rate: Used to identify slow-moving and fast-moving products
•	Stock level categorization: Grouping products by low, mid, and high stock levels
•	ABC Analysis: Used to categorize products
## 5.	Geographical Distribution Analysis
The geographical spread of warehouses across the 10 countries was mapped using latitude and longitude data to observe the distribution patterns and potential logistical inefficiencies.
## 6.	Tools Used 
The analysis was conducted using:
•	Power BI
•	Excel
•	Basic statistical functions
•	Data visualization for better insight communication
# ANALYSIS AND RESULT
## 1.	Stock Quantity Distribution 
An initial exploratory analysis of the stock_quantity column revealed that the majority of products fall into the mid stock level, accounting for 40.42% of all items. However, when analyzing the total quantity of stock across levels, the high stock level holds the largest volume — with approximately 1,267,600 units, despite only 29.76% of products belonging to this category.
In contrast, 28.83% of products are categorized as low stock, representing a total of 227,697 units. Notably, 262 products within this group are considered understocked (stock quantity < reorder point), suggesting a potential risk of stockouts for those items.

 
These findings suggest that the company may be overstocking products with potentially lower demand, which can lead to increased storage costs and a higher risk of obsolescence. On the other hand, the understocking observed in the low stock category highlights the need for tighter inventory control and more responsive restocking mechanisms for critical items.

## 2.	Inventory Turnover Rate
The inventory turnover rate was assessed across product categories by analyzing stock quantity relative to lead time (in days). This metric estimates how many units are held in stock per day of replenishment time, offering insight into how efficiently each category moves inventory.

 

Most product categories recorded a turnover rate between 62 and 75 units per day, with an average of 68.68 units/day.

•	Clothing had the highest turnover rate at 74.25, indicating that it has the most efficient stock movement relative to lead time. This suggests that clothing products are in higher demand or are restocked more responsively — warranting more frequent reordering to avoid stockouts.
•	Office Supplies had the lowest turnover rate at 62.37, making it the least efficient category in terms of inventory movement. This may require a review of demand forecasting or stocking strategy for this group.

