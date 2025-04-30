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
## 3.	ABC Analysis
An ABC analysis was conducted to classify products based on their contribution to overall inventory value:
•	Group A (high value, moderate quantity, monitor closely): 34.44% of products
•	Group B (moderate value): 24% of products
•	Group C (low-impact products, largest number of products): 41.56%

 
This distribution highlights that Group A products, while fewer in number, contribute the most to inventory value and should be monitored closely with tighter controls and forecasting. Group B products require moderate oversight, as they play a balanced role in value and quantity. Group C products, which make up the largest share by count but the lowest by value, may benefit from simplified management strategies, such as bulk handling or periodic reviews, to reduce operational costs.

## 4.	Geographic Distribution
The inventory is distributed across 5,000 warehouse locations in 10 European Countries. The distribution of stock is relatively balanced, with Germany holding the largest share at 11.05%, followed closely by Spain (10.59%), Belgium (10.46%), Poland (10.44%) and United Kingdom (10.04%). 
  

 
This even spread suggests that inventory is strategically allocated across region, likely to minimize lead times and optimize fulfillment. The fairly uniform distribution may also reflect an attempt to keep warehouses in proximity to major markets or customer hubs, ensuring product availability and reducing shipping costs. 

## 5.	Restocking and Lead Time
The average lead time across all suppliers was approximately 14.96 days, indicating a typical two-week wait between order and fulfillment. However, some supplier exhibited notable variance:
•	SUP041, SUP020, and SUP032 had an average lead time of 17 days 
•	SUP002 followed closely at 16 days
	These inconsistencies can complicate reorder planning and increase the risk of stockouts 	or inventory imbalances, especially for fast-moving products.
	In terms of restocking activity, the month of May recorded the highest number of 	restocks, with 462 restock events totaling 245,261 units. October followed closely with 	457 restocks and 227,802 units.
	This trend suggests a seasonal restocking pattern, with the spring months (March–May) 	seeing the highest restocking volumes, likely due to increased demand or post-winter 	inventory rebuilding. A secondary peak occurs in the fall months (September–	November), potentially preparing for year-end demand surges.
	               
	 
## 6.	Cost and Pricing Analysis
An analysis of product pricing revealed the top five most expensive items, which span across various categories: Home & Garden, Electronics, Office Supplies, Books, and Clothing. These products command the highest unit prices in the inventory, yet notably, they are maintained at moderate to high stock levels.
 

This indicates that the company is confident in the turnover potential of these high-value items or considers them strategically important (e.g., premium offerings, customer demand drivers). Maintaining sufficient stock for these items could help ensure availability for high-margin sales and reduce lost revenue from out-of-stock situations.
At the same time, it's important to monitor whether holding costs for these expensive products are justified by their sales velocity, especially if they are slower-moving. A periodic cost-to-benefit analysis of high-priced SKUs could support better capital allocation.	
# CONCLUSION
This inventory analysis provided key insights into the company's operational strengths and areas for optimization. The evaluation of stock levels revealed a concentration of inventory in high-stock categories, suggesting potential overstocking and increased holding costs. Simultaneously, understocked items within the low stock level category highlight risks of stockouts and lost sales opportunities.
The turnover analysis showed clear differences in efficiency across product categories, with Clothing exhibiting the highest turnover and Office Supplies the lowest — pointing to the need for category-specific replenishment strategies. The ABC classification further emphasized that a relatively small portion of products (Group A) accounts for a significant share of inventory value, warranting focused monitoring and resource allocation.
Seasonal trends in restocking activity — peaking during spring and fall — alongside variations in supplier lead times, underscore the importance of timely procurement planning. The geographic distribution of stock appears well-balanced across European warehouses, likely supporting regional demand and reducing delivery lead times.
Lastly, the cost and pricing analysis highlighted that high-value products are being stocked at healthy levels, which may reflect strategic positioning but also necessitates ongoing assessment of demand and turnover to avoid capital inefficiency.
Overall, this analysis supports more informed decision-making around inventory control, supplier coordination, and stock prioritization. Applying the insights from this report can lead to improved inventory performance, reduced costs, and stronger supply chain resilience.
# RECOMMENDATION
Based on the insights uncovered in this inventory analysis, the following strategic recommendations are proposed to improve inventory efficiency, reduce costs, and support better demand responsiveness:
1.	Reduce Overstocking in High Stock Level Categories
•	Conduct a product-level demand review to identify slow-moving items.
•	Implement stock threshold alerts and automated restocking limits to prevent overstock accumulation.
•	Consider markdown strategies or promotional campaigns to reduce excess inventory.
2.	Address Understocked and At-Risk Products
•	Prioritize replenishment of the 262 understocked products that fall below reorder points.
•	Reevaluate reorder levels for low-stock items based on actual demand and lead time variability.
•	Set up predictive restocking models using historical consumption trends.
3.	Tailor Replenishment Frequency by Category Performance
•	Increase reorder frequency for high-turnover categories like Clothing to avoid lost sales.
•	Monitor low-turnover categories (e.g., Office Supplies) for potential overstock and space inefficiency.
•	Introduce category-specific inventory KPIs to guide restocking behavior.
4.	Optimize ABC Inventory Control
•	Apply strict monitoring and forecasting to high-value Group A items.
•	Streamline bulk ordering and automate controls for Group C items to reduce handling and cost.
•	Reassess product categorization periodically as demand and pricing evolve.
5.	Improve Supplier and Lead Time Planning
•	Engage with suppliers with high lead time variance (e.g., SUP041, SUP020) to understand delays and negotiate performance improvements.
•	Incorporate supplier reliability into reorder models to avoid timing mismatches.
6.	Align Inventory Planning with Seasonal Demand Trends
•	Use insights from peak restocking months (e.g., May and October) to preemptively adjust stock levels.
•	Integrate seasonal patterns into demand forecasting tools to smooth procurement cycles.
7.	Monitor High-Value Product Performance
•	Regularly assess the turnover rate of high-priced items to ensure capital is not tied up in low-demand stock.
•	Balance premium product availability with cost control measures like dynamic safety stock.


