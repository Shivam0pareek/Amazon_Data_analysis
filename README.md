📊 Amazon Brazil Market Analysis — SQL Project for Amazon India
📝 Project Overview
This project involves analyzing Amazon Brazil’s e-commerce data to extract key insights that can be leveraged by Amazon India to improve operations, marketing, and customer experience.

You will work with a dataset that spans customers, orders, products, sellers, payments, and more. The analysis is divided into three stages, covering:

Basic SQL

Joins & Aggregations

Window Functions & CTEs

🎯 Objectives
Identify customer behavior patterns, sales trends, and payment preferences.

Understand product performance and revenue growth across time and segments.

Create customer segmentations for marketing and loyalty programs.

Provide actionable insights and visualizations for Amazon India.

🧱 Database Schema
The dataset contains 7 tables:

Table Name	Description
customers	Customer details including location and unique IDs
orders	Order status and timestamp details
order_items	Product-level information within orders
products	Product metadata like name, category, and price
sellers	Seller information and location
payments	Payment types and transaction values
geolocation	(Optional) Used for mapping delivery distance analytics

Relationships:

orders.customer_id → customers.customer_id

order_items.order_id → orders.order_id

order_items.product_id → products.product_id

order_items.seller_id → sellers.seller_id

payments.order_id → orders.order_id

🛠️ Setup Instructions
1. Prepare Your Environment
Use PostgreSQL and pgAdmin.

Create a database:

sql
Copy
Edit
CREATE DATABASE amazon_analysis;
Create a schema:

sql
Copy
Edit
CREATE SCHEMA amazon_brazil;
2. Import CSV Files
Download and extract Excel sheets

Save each sheet as a separate .csv file:

customers.csv

orders.csv

order_items.csv

products.csv

sellers.csv

payments.csv

Use pgAdmin > Table Import/Export Tool to load each CSV file into corresponding tables.

Make sure to set appropriate primary keys and foreign keys as per schema.

📊 Analysis Breakdown
✅ Analysis I – Fundamentals
Standardize and round payment averages

Identify popular payment types

Find products in specific price ranges

Discover top revenue-generating months

Analyze price gaps by category

Determine consistent payment types

Find missing/incomplete product categories

🔁 Analysis II – Aggregations & Joins
Payment types by order value segment

Price analysis for each product category

Multi-order customers

Customer loyalty classification

Top 5 categories by revenue

🧠 Analysis III – Advanced (CTE & Window Functions)
Seasonal sales comparison

Products with above-average sales

Monthly revenue trends (2018)

Customer loyalty segmentation via CTE

Top 20 high-value customers

Monthly cumulative product sales (Recursive CTE)

MoM growth by payment type (Window + LAG)

📁 Files Included
File Name	Description
amazon_analysis.sql	All SQL queries used for analysis with comments
Amazon_Insights_Report.docx	Screenshots of queries + insights & recommendations
csv/ folder	Contains cleaned and formatted CSV files for each table

📌 Submission Guidelines
Submit .sql file with all queries (with comments).

Include screenshots of each query and a brief explanation in the Word document.

Export revenue trend and loyalty segment graphs from Excel for relevant questions.

Focus on clear structure, optimized queries, and accurate insights.

💡 Pro Tips
Use ROUND(), CASE, JOIN, GROUP BY, CTE, WINDOW functions efficiently.

Label each query with a comment block for clarity.

Use Excel visualizations where applicable (e.g., line chart, pie chart).

🙌 Final Note
This project mimics real-world business analytics and will enhance your SQL, data modeling, and critical thinking skills. Don’t hesitate to make assumptions where necessary and document them in your submission.

Happy analyzing! 🚀
