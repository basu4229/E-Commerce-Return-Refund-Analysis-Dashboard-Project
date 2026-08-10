📦 E-Commerce Return & Refund Analysis — Power BI
📌 Project Overview

Returns and refunds can have a major impact on e-commerce profitability. A high return rate doesn't only mean lost sales — it can also increase reverse-logistics costs, inventory issues, refund exposure, and customer dissatisfaction.

This Power BI project analyzes e-commerce orders, returns, refund amounts, return reasons, product categories, sales channels, discounts, and return duration to understand where returns are happening and what factors may be contributing to them.

The dashboard is designed to help business teams quickly identify high-return categories, problematic products, major return reasons, and potential relationships between discounts and return rates.

🎯 Business Problem

The business wanted to answer questions such as:

How many orders are being returned?
What is the overall return rate?
How much money is being refunded?
Which product categories generate the most returns?
Which return reasons contribute most to returned units?
Which sales channels have higher return volumes?
Are heavily discounted products more likely to be returned?
Which products require closer investigation?
How long does it typically take for customers to return products?
Where should the business focus its return-reduction efforts?
📊 Dashboard Pages
1. Executive Summary

The executive page provides a high-level view of return and refund performance.

Key KPIs include:

Total Orders
Return Orders
Return Rate %
Refund Amount
Returned Units
Refund Amount Trend
Returns by Sales Channel
Returns by Category
Return Reason Pareto Analysis

This page is intended for management to understand the overall return situation without going through individual products.

2. Product Diagnostics

The second page goes deeper into product-level return behavior.

It includes:

Top Return Category
Top Return Reason
Average Return Days
Discount vs Return Rate analysis
Return reason heatmap by subcategory
Product-level return performance table
Total Orders
Returned Units
Return Rate %
Refund Amount
Average Return Days
Average Discount %

This page helps identify products and subcategories that may require operational or product-level action.

🔎 Key Findings

Based on the dashboard:

1. Return rate is significant

The dashboard shows 3,100 total orders and 745 return orders, resulting in a 24.03% return rate.

That means roughly 1 out of every 4 orders is being returned, making returns an important business area to investigate.

2. Refund exposure is substantial

The total refund amount shown is approximately 3.82M, indicating that returns are not only an operational issue but also have a direct financial impact.

3. Fashion is the leading return category

Fashion appears as the top return category, with the highest returned-unit volume among the categories displayed.

This makes fashion a natural starting point for investigating issues such as sizing, product expectations, quality, and product descriptions.

4. Product expectations are a major return driver

"Product Not As Expected" is identified as the top return reason.

This could indicate a gap between what customers expect before purchase and what they receive.

Possible areas to investigate include:

Product images
Product descriptions
Size information
Product specifications
Customer reviews
Product quality
Customer expectations created by marketing
5. Some return reasons dominate overall returns

The Pareto analysis shows that a relatively small number of return reasons contribute a large proportion of returned units.

This is useful because the company doesn't necessarily need to solve every return reason at once. It can prioritize the biggest contributors first.

6. Discounts and returns deserve attention

The scatter plot comparing Average Discount % vs Return Rate % shows variation across products.

Some products have relatively high discounts alongside higher return rates. This doesn't prove that discounts cause returns, but it highlights products that deserve further investigation.

7. Product-level performance varies considerably

The product diagnostics table shows noticeable differences in:

Return rate
Returned units
Refund amount
Average return days
Average discount

This suggests that return management should not be approached only at an overall business level. Specific products may require targeted action.

💡 Business Takeaways

The analysis suggests several practical actions:

Reduce "Product Not As Expected" returns

Improve product information with better photography, detailed specifications, accurate descriptions, size guides, and customer reviews.

Focus on Fashion first

Since Fashion has the highest return volume, it should be one of the first categories investigated.

Prioritize the biggest return reasons

Use the Pareto analysis to focus resources on the return reasons responsible for the largest share of returns.

Investigate high-discount products

Products with both high discounts and high return rates should be reviewed to understand whether promotions are attracting customers whose expectations don't match the product.

Monitor problematic products

Products with unusually high return rates should be reviewed individually rather than relying only on category-level averages.

Improve return-cycle management

Average return days can help operations teams understand how quickly returned inventory is coming back into the business.

🛠️ Tools & Technologies
Power BI
DAX
Power Query
Data Modeling
Data Cleaning & Transformation
Interactive Visualizations
Power BI Techniques Used
KPI Cards
Slicers
Date filtering
Donut Chart
Bar Chart
Pareto Analysis
Heatmap / Matrix
Scatter Plot
Detailed Product Table
Conditional Formatting
Time-Series Analysis
DAX Measures
*Dataset Taken from Kaggle.com 
📁 Dashboard Structure
E-Commerce Return & Refund Analysis
│
├── Executive Summary
│   ├── Total Orders
│   ├── Return Orders
│   ├── Return Rate
│   ├── Refund Amount
│   ├── Refund Trend
│   ├── Returns by Sales Channel
│   ├── Returns by Category
│   └── Return Reason Pareto
│
└── Product Diagnostics
    ├── Top Return Category
    ├── Top Return Reason
    ├── Average Return Days
    ├── Discount vs Return Rate
    ├── Return Reason Heatmap
    └── Product-Level Analysis
📌 Conclusion

This project goes beyond simply reporting return numbers. The objective was to turn transaction-level return data into business insights that can support better decisions around products, customers, promotions, and return management.
Screenshot Image :

The biggest opportunity is to understand why customers return products and then focus improvement efforts on the categories, products, and return reasons creating the greatest financial and operational impact.<img width="1907" height="1768" alt="E-Commerce Return   Refund Analysis Screenshot" src="https://github.com/user-attachments/assets/8a1a3fbb-be68-466e-a2b8-2b1a67f1f5bb" />
