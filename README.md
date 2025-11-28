# Ecomerce-Trend-Analysis-Using-SQL
E-commerce Trends Analysis using SQL — A data-driven study of sales, customers, and operational performance using SQL queries, views, and analytics.


📦 E-Commerce Trends Analysis Using SQL
This project was completed as part of my internship training at Imarticus Learning, where I worked on analysing an e-commerce dataset using SQL.
The purpose of the project was to understand how data-driven insights can support business decisions in areas like sales, customer behaviour, product performance, and daily operations.
This project gave me real hands-on experience with SQL and business analytics used in real companies.

⭐ Project Overview
During this internship assignment, I analysed a structured e-commerce database and answered key business questions, such as:

Which products sell the most?

Who are the top customers?

How long does delivery take?

Which discounts are effective?

What are the monthly order trends?

By using SQL joins, grouping, aggregation, conditions, and views, I was able to generate meaningful insights.

🗂 Database Structure
The database contains multiple tables that represent real e-commerce operations:

Users – login and roles

Customers – customer details

Products – item information

Orders & OrderDetails – purchase history

Coupons & OrderCoupons – discounts used

ProductReviews – ratings and reviews

Shipments – delivery status and timelines

Cart – temporary selection before order

This schema allowed complete analysis of sales, customers, and logistics.

🔍 Key Insights & SQL Queries
1. Sales Trends

Identified top-performing products and overall sales performance.

SELECT P.ProductName, SUM(OD.Quantity) AS TotalSold
FROM OrderDetails OD
JOIN Products P ON OD.ProductID = P.ProductID
GROUP BY P.ProductName
ORDER BY TotalSold DESC
LIMIT 5;

2. Customer Insights

Analysed purchasing patterns and highest-spending customers.

SELECT C.Name, SUM(O.TotalAmount) AS TotalSpent
FROM Customers C
JOIN Orders O ON C.CustomerID = O.CustomerID
GROUP BY C.Name
ORDER BY TotalSpent DESC
LIMIT 5;

3. Pricing & Discounts

Studied discount strategies and categorised products by price.

SELECT ProductName,
CASE
    WHEN Price < 100 THEN 'Budget'
    WHEN Price BETWEEN 100 AND 500 THEN 'Mid-range'
    ELSE 'Premium'
END AS PriceCategory
FROM Products;

4. Shipment & Delivery Trends

Evaluated carrier performance and delivery timelines.

SELECT Carrier, COUNT(ShipmentID) AS TotalShipments
FROM Shipments
GROUP BY Carrier;

📈 Skills Learned During Internship

Through this project at Imarticus Learning, I gained hands-on experience in:

Writing industry-level SQL queries

Analysing structured business datasets

Understanding joins, views, and aggregations

Solving real e-commerce business problems

Presenting findings with SQL results

Improving analytical thinking and problem-solving


📎 Project File

The complete project presentation is available in this repository:
Final Ecommerce Trends Analysis PPT.pptx

🏁 Conclusion

This internship project helped me understand how SQL is used in real-world business environments.
It strengthened my skills in analysing sales data, customer behaviour, product performance, and logistics to support better decision-making in an e-commerce system.
