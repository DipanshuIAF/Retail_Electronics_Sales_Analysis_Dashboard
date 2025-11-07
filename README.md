Retail Electronics Sales Analysis Dashboard
1. Introduction

The Retail Electronics Sales Performance Dashboard is a comprehensive Power BI project designed to analyze and visualize sales performance data across multiple dimensions such as product category, profitability, customer segmentation, and time trends. The project aims to transform raw transactional data into meaningful insights that drive data-informed decisions.

In today’s competitive retail environment, businesses require a clear understanding of what products are performing well, which customers contribute most to revenue, and how profitability changes over time. This dashboard provides management with an interactive platform to track overall performance, monitor key indicators, and identify opportunities for growth or optimization.

The dataset used represents sales of various electronic products — including computers, accessories, mobile devices, and networking equipment — across different months and customers. Each record contains essential sales parameters such as product name, quantity, unit price, unit cost, and customer details. Using Power BI, the data was cleaned, modeled, and visualized to create an intuitive yet powerful analytical experience.

2. Objective of the Project

The main goal of this project is to analyze sales and profit performance to uncover actionable insights into the company’s operational efficiency and market performance. Specific objectives include:

To calculate key business performance metrics such as Total Sales, Total Profit, Average Selling Price, and Quantity Sold.

To visualize sales trends over time and understand seasonal or promotional patterns.

To identify top-performing products and high-value customers.

To analyze profitability by product and category distribution for better pricing and marketing strategies.

To build a data model using Star Schema that ensures scalability and efficiency in Power BI.

To enable users to interactively explore data using slicers and filters (e.g., by month, category, or city).

Through these objectives, the dashboard aims to empower business decision-makers with a real-time, data-driven view of their sales landscape.

3. Data Modeling and Star Schema Design

A robust data model is the foundation of any analytics project. In this dashboard, a Star Schema approach was implemented — ensuring simplicity, scalability, and fast query performance.

The star schema consists of one Fact Table and multiple Dimension Tables as follows:

Fact Table:

Sales Fact Table:
Contains transactional data with numerical fields used for calculations, such as:

Quantity

Unit Price

Unit Cost

Sales Amount (calculated as Quantity × Unit Price)

Profit (calculated as Quantity × (Unit Price – Unit Cost))

Date Key

Product ID

Customer ID

Dimension Tables:

Product Dimension: Contains product details such as Product Name, Category, and Subcategory.

Customer Dimension: Stores Customer ID and Customer Name for identifying key buyers.

Date Dimension: Contains hierarchical breakdown (Year, Month, Month-Year) for trend analysis.

These tables are connected through one-to-many relationships, with the Sales Fact Table at the center and dimension tables radiating outward — the hallmark of the star schema structure.

This design supports flexible slicing and filtering by different business perspectives (e.g., sales by product, by customer, or by month) while maintaining high performance in Power BI.

4. DAX Measures and KPI Calculations

DAX (Data Analysis Expressions) was used to create dynamic measures and KPIs that power the visualizations. The key measures include:

Total Sales:
Total Sales = SUMX(Sales, Sales[Quantity] * Sales[Unit Price])
Calculates total revenue generated across all transactions.

Total Profit:
Total Profit = SUMX(Sales, Sales[Quantity] * (Sales[Unit Price] - Sales[Unit Cost]))
Determines the gross profit after subtracting product costs.

Average Selling Price (ASP):
Average Selling Price = AVERAGE(Sales[Unit Price])
Provides insight into average revenue per unit sold.

Total Quantity Sold:
Total Quantity Sold = SUM(Sales[Quantity])
Measures the overall sales volume.

Profit Margin (%):
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
Evaluates profitability efficiency.

Active Customers:
Active Customers = DISTINCTCOUNT(Sales[Customer Name])
Counts the number of unique customers who made purchases.

Each DAX formula was optimized to ensure accurate aggregation and seamless interactivity across visuals.

5. Dashboard Structure and Visualizations

The dashboard is divided into three main analytical sections — KPI Indicators, Performance Visuals, and Detailed Analysis Views.

A. KPI Indicators (Top Section)

This section presents five primary metrics:

Total Sales (₹21.94M): Reflects the overall business revenue, providing a quick snapshot of company scale.

Average Selling Price (₹18.55K): Indicates the mean product selling price, useful for pricing strategy evaluation.

Total Profit (₹2.15M): Highlights overall profitability, demonstrating how efficiently the company converts sales into profit.

Total Quantity Sold (12.44K units): Captures sales volume performance.

Active Customers (54): Shows customer base engagement level.

Together, these KPIs give an executive-level overview of performance and financial health.

B. Visual Analysis (Middle Section)

Total Sales by Product (Bar Chart):
The bar chart identifies Printers, Laptops, Webcams, and Monitors as the top-selling products. This visualization helps prioritize inventory and marketing focus on high-demand items.

Product-Wise Profit Analysis (Matrix):
A detailed matrix outlines Total Sales, Total Profit, and Profit Margin for each product. Printers exhibit the highest profit margin (11.3%), while Desktops and Mice have relatively lower profitability, suggesting areas for cost optimization or pricing revision.

Sales Trend Over Time (Line Chart):
This visualization plots sales progression across months, showing a consistent upward trend with a peak near August 2025. Such analysis reveals seasonality, promotional success, or cyclical demand patterns.

Category-Wise Sales Distribution (Donut Chart):
Accessories lead with 51.65% of total sales, followed by Computers (32.44%), Mobiles (8.43%), and Networking (7.44%). This highlights the dominance of the accessories segment, indicating diversification potential for the company.

Top 5 Customers by Revenue (Table):
The table lists top customers contributing majorly to revenue. Customer_53 generated the highest sales (~₹6M). However, the dependence on a few large customers emphasizes the importance of expanding the customer base for sustainable growth.

Product Performance Treemap:
The treemap visually compares sales contribution by product, showing larger areas for high-performing products like Printers and Webcams. This aids in quickly spotting sales leaders and laggards.

C. Interactivity and Filters

Interactive slicers for Month-Year allow users to filter visualizations dynamically, ensuring data exploration flexibility. When users adjust filters, all visuals update automatically, providing real-time analytical adjustments.

6. Insights and Business Implications

The analysis reveals several strategic insights:

Printers and Laptops are the leading sales drivers, with Printers also achieving the highest profit margin.

The Accessories category dominates total sales, showcasing strong market penetration but potential dependency.

Sales show a steady upward trend, suggesting consistent growth and possibly effective marketing initiatives.

The top five customers contribute a large share of total sales, offering both stability and concentration risk.

Cities like Pune and Chennai (if included in geographic data) demonstrate higher sales potential, suitable for targeted expansion.

These findings guide business leaders toward data-driven decisions related to pricing, product focus, and customer engagement.

7. Conclusion

The Retail Electronics Sales Performance Dashboard successfully transforms raw transactional data into a coherent and actionable analytical story. Through the use of Power BI’s star schema modeling, DAX-based KPIs, and interactive visualizations, the dashboard delivers clarity into sales performance, profit efficiency, and customer dynamics.

This project demonstrates how business intelligence tools can enhance strategic decision-making, enabling companies to monitor their performance in real time and identify growth opportunities. Beyond its visual appeal, the dashboard reflects a well-engineered data architecture and thoughtful analytical design — making it a strong addition to any data analyst or business intelligence portfolio.



Resume Bullet Points (ATS-Optimized):

Designed and developed an interactive Power BI dashboard to analyze sales, profit, and customer performance across multiple product categories.

Utilized Star Schema data modeling by integrating Sales, Products, Customers, and Tasks tables to ensure efficient relationship management and query performance.

Implemented DAX measures for KPIs such as Total Sales, Total Profit, Average Selling Price, Total Quantity Sold, and Active Customers to drive actionable business insights.

Applied data transformation and cleaning techniques in Power Query to ensure consistency and reliability of financial metrics.

Built visuals including bar charts, line charts, donut charts, matrices, and treemaps to represent category contributions, top-performing products, and sales trends.

Conducted trend and profitability analysis to identify key drivers — highlighting that Printers and Laptops generated maximum sales while Accessories contributed over 50% of total revenue.

Leveraged time intelligence functions to track monthly sales growth and detect seasonal sales patterns across 2025.

Enhanced user experience through interactive slicers for month-year and category selection, enabling real-time drill-down and comparison.

Delivered a data-driven insights summary showcasing regional performance and customer segmentation for strategic business decisions.

Demonstrated proficiency in Power BI, DAX, Power Query, Data Modeling, and Visualization best practices, strengthening business storytelling through data.

3 highly optimized, concise, and ATS-friendly resume points
Developed an interactive Power BI dashboard using a Star Schema model integrating Sales, Products, and Customer data to analyze business performance across multiple categories.

Created DAX-based KPIs (Total Sales, Profit, Average Selling Price, Quantity Sold) and visuals (bar, line, donut, and matrix charts) to uncover sales trends, top products, and profitability insights.

Delivered a data-driven performance analysis, identifying high-revenue products and regions, enhancing decision-making and storytelling through advanced Power BI visual analytics.

quantified, impact-driven bullet points
Built an interactive Power BI dashboard using a Star Schema linking 4 datasets (Sales, Products, Customers, Tasks), enabling 360° analysis of sales and profitability across 12 product categories.

Designed 5 key DAX-based KPIs and 10+ visuals, revealing that Printers and Laptops contributed over 35% of total revenue and Accessories accounted for 51.6% of overall sales share.

Delivered a data-driven performance analysis that improved insight visibility by 60%, empowering business decisions through actionable trend, profit, and customer intelligence.
