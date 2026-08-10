📊 E-Commerce Return & Refund Analysis — Power BI
📌 Project Overview

Returns are a normal part of e-commerce, but when return volume starts increasing, it can quickly affect revenue, inventory, logistics, and customer experience.

I built this Power BI project to look beyond the number of returned orders and understand what is driving returns, where the refund exposure is coming from, and which areas deserve business attention first.

The report uses an order-line dataset and follows a beginner-friendly star schema, allowing the analysis to cover everything from overall return performance to individual product-level return behavior.

The main objective was simple:

Turn return and refund data into insights that can support practical business decisions.

🎯 Business Problem

The business needs to understand the scale and causes of product returns.

Instead of creating KPIs just for reporting purposes, each KPI in this dashboard is connected to a specific decision question.

KPI	Business Question	Decision Lens
Total Orders	How large is the order base?	Business Volume
Returned Orders	How many orders came back?	Return Exposure
Return Rate %	What share of orders were returned?	Operational Risk
Refund Amount	How much money was refunded?	Financial Leakage
Average Return Days	How quickly are products returned after delivery?	Customer Behavior
Products Returned	How many products were affected?	Product Spread
Top Return Category	Which category creates the most returned units?	Priority Area
Top Return Reason	What is the biggest reason behind returns?	Action Trigger

This approach keeps the dashboard focused on decisions rather than just visualizations.

🗂️ Dataset & Data Model

The project starts with a raw order-line table where:

One row represents one product line inside an order.

Fact Table

Fact_Orders

The fact table contains information such as:

Order ID
Order Date
Delivery Date
Customer ID
Product ID
Quantity
Unit Price
Discount %
Return Flag
Return Quantity
Sales Channel
Payment Method
Return Reason
Dimension Tables

The model contains separate dimensions for:

Date
Products
Customers
Sales Channel
Payment Method
Return Reason

This creates a clean and manageable star-schema model for analysis.

Derived Calculations

Several business metrics were created inside Power BI using DAX, including:

Refund Amount
Return Days
Return Rate %
Month-over-Month calculations
Return Reason Ranking
Cumulative Return %
Pareto analysis
Dynamic Top Category
Dynamic Top Return Reason
Product Risk indicators
📄 Dashboard Structure
1️⃣ Executive Summary

The first page provides a high-level view of the overall return and refund situation.

Key KPIs
Total Orders: 3,100
Returned Orders: 745
Return Rate: 24.03%
Refund Amount: 3.82M

The KPI cards also include MoM indicators, making it easier to understand whether performance is improving or moving in the wrong direction.

Monthly Return Trend

The trend visual combines returned orders and return rate over time.

This helps identify:

Monthly spikes
Changes in return behavior
Potential seasonality
Periods requiring further investigation
Returns by Category

This visual shows which product categories contribute the most returned units.

Rather than simply asking "How many returns do we have?", the analysis asks:

"Which categories are creating the biggest return problem?"

Return Reason Pareto

The Pareto analysis ranks return reasons by returned units and adds a cumulative percentage.

This helps identify the vital few reasons responsible for a large portion of returns, allowing the business to prioritize corrective action.

Returns by Sales Channel

Returned units are also analyzed across:

Website
Mobile App
Marketplace
Offline Store

This helps identify where return volume is concentrated and whether certain channels require additional investigation.

Filters

The Executive Summary can be explored using:

Date Range
Category
Sales Channel
Reset Filters
2️⃣ Product Diagnostics

The second page moves from "What is happening?" to "Why is it happening?"

This page focuses on root-cause and product-level analysis.

Key Diagnostic KPIs
Average Return Days: 14.9 days
Products Returned: 104 unique products
Top Category: Fashion
Top Reason: Product Not As Expected
Return Reason Heatmap

A subcategory-by-return-reason heatmap highlights where specific problems are concentrated.

For example, the business can quickly identify whether issues such as:

Wrong Size
Damaged Product
Defective Product
Late Delivery
Product Not As Expected
Quality Issue
Wrong Item
Changed Mind

are concentrated within particular subcategories.

This is much more useful than looking at the overall return rate alone.

Discount vs Return Risk

The scatter plot compares:

Average Discount % vs Return Rate %

The purpose isn't to claim that discounts automatically cause returns.

Instead, it helps identify products where high discount levels and high return rates appear together, creating a potential risk area for further investigation.

Low-volume products are excluded from the risk analysis so that products with very little activity don't create misleading conclusions.

Product Return Details

The detailed product table provides:

Product
Subcategory
Total Orders
Returned Units
Return Rate %
Refund Amount
Average Return Days
Average Discount %

This gives the business a way to move from an overall dashboard view into specific products that may require attention.

📐 Analytical Techniques Used

This project focuses heavily on the analytical layer rather than simply creating attractive visuals.

🔹 MoM Analysis

Previous-month calculations are used to show movement in KPI performance.

Directional arrows are displayed below KPI cards to make the change easier to interpret.

🔹 Pareto Analysis

Return reasons are ranked and converted into cumulative percentages to identify the few causes responsible for the largest share of returned units.

🔹 Heatmap Analysis

A subcategory × return-reason matrix uses conditional formatting to highlight high-intensity problem areas.

🔹 Product Risk Analysis

Product return rates are compared against a benchmark to identify potential high-risk products.

🔹 Dynamic KPIs

TOPN-based DAX measures dynamically identify:

Top Return Category
Top Return Reason

These values respond to the selected filters.

🔹 Volume Filtering

Low-volume products are removed from risk-focused visuals to reduce the chance of drawing conclusions from insufficient data.

🔎 Key Findings

The dashboard highlights several areas worth investigating.

1. Returns represent a significant operational issue

With 3,100 orders and 745 returned orders, the return rate stands at 24.03%.

That means returns represent a substantial portion of the order base and should be treated as a business-performance issue rather than only a customer-service metric.

2. Refunds create meaningful financial exposure

The dashboard reports approximately 3.82M in refund amount.

This makes it important to prioritize return causes not only by volume but also by their financial impact.

3. Fashion is the primary return category

Fashion is currently the top return category by returned units.

This makes it a logical starting point for investigating issues such as sizing, product expectations, quality and product information.

4. "Product Not As Expected" is the leading return reason

This finding points toward a possible gap between the customer's expectation at purchase and the actual product received.

Product imagery, descriptions, specifications, reviews and expectation-setting should therefore be reviewed.

5. Return causes are not equally important

The Pareto analysis demonstrates why looking at every return reason equally isn't necessarily efficient.

The business can focus first on the reasons contributing the largest share of returned units.

6. Discounting needs to be monitored

Some products show a combination of relatively high discounts and higher return rates.

This doesn't establish causation, but it creates a useful risk signal for further product and promotion analysis.

💡 Business Recommendations

The dashboard can translate directly into operational actions.

🛍️ Product Not As Expected

Improve:

Product photography
Product descriptions
Product specifications
Product comparison information
Customer reviews

The goal is to make the online product experience closer to the actual product.

👕 Wrong Size

For Fashion and Footwear:

Improve size guides
Add measurement references
Show fit information
Analyze size-related return feedback
📦 Damaged Product

Review:

Packaging standards
Warehouse handling
Delivery partners
Marketplace fulfillment processes
⭐ Quality Issues

Create vendor-level scorecards using:

Returned units
Return rate
Refund amount
Quality-related return reasons

This can help identify suppliers contributing disproportionately to returns.

💰 Discount Risk

Avoid aggressive discounts on products that already show a high return rate unless there is a clear business reason.

Promotions should be evaluated against both sales volume and post-sale return behavior.

🎯 Prioritization Rule

A useful business rule from this analysis is:

Prioritize return causes that combine high returned-unit volume with high refund exposure.

This prevents the business from focusing only on the number of returns while ignoring their financial impact.

🛠️ Tools & Technologies

Power BI
DAX
Power Query
Data Modeling
Data Cleaning
Data Visualization
Star Schema

Power BI Features Used
KPI Cards
Slicers
Conditional Formatting
Matrix Heatmap
Scatter Plot
Pareto Chart
Donut Chart
Bar Chart
Line/Area Trend
Dynamic DAX Measures
MoM Analysis
Interactive Filtering
📚 What I Learned From This Project

One of the main goals of this project was to build something that demonstrates more than Power BI visualization skills.

The project helped bring together:

Data Cleaning → Data Modeling → DAX → Business Logic → Visualization → Business Recommendations

The biggest learning for me was that a good dashboard shouldn't answer only:

"What happened?"

It should also help answer:

"Why did it happen, and what should the business do next?"

📁 Suggested GitHub Repository Structure
E-Commerce-Return-Refund-Analysis/
│
├── README.md
│
├── Dataset/
│   └── ecommerce_orders.csv
│
├── PowerBI/
│   └── E-Commerce_Return_Refund_Analysis.pbix
│
├── Dashboard/
│   ├── Executive_Summary.png
│   └── Product_Diagnostics.png
│
├── DAX/
│   └── Measures.md
│
└── Documentation/
    └── Business_Insights.md
Screenshot Image :

The biggest opportunity is to understand why customers return products and then focus improvement efforts on the categories, products, and return reasons creating the greatest financial and operational impact.<img width="1907" height="1768" alt="E-Commerce Return   Refund Analysis Screenshot" src="https://github.com/user-attachments/assets/8a1a3fbb-be68-466e-a2b8-2b1a67f1f5bb" />
