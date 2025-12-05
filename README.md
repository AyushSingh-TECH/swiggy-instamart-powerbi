# 🛍️ Swiggy Instamart – Power BI Analytics Dashboard  

A complete end-to-end **Sales & Delivery Analytics Dashboard** built using **Power BI**, focusing on business insights such as sales performance, product trends, customer behavior, delivery efficiency, store operations, and revenue metrics.

---

## 📌 Project Overview

This dashboard helps analyze and monitor key business performance areas including:

- 📦 Total Orders & Revenue Trends  
- 🛒 Best-Selling Products & Categories  
- 🏬 Store & City-level Sales Insights  
- 🚚 Delivery Metrics (On-time %, Late Deliveries, Partner Performance)  
- 💳 Payment Behavior & Promo Code Usage  

The purpose of this project is to simulate a real business analytics case and convert raw data into actionable insights for decision-makers.

---

## 🧱 Data Model (Star Schema)

This project uses a **Star Schema Model** for optimized analytical reporting.

| Table Name | Type | Description |
|-----------|------|-------------|
| Orders | Fact | Contains sales & delivery transaction details |
| Products | Dimension | Product category, name, and pricing |
| Customers | Dimension | Customer demographics |
| Stores | Dimension | Store location details |
| DeliveryPartners | Dimension | Rider and delivery information |
| DateDim | Dimension | Enables time intelligence |

📁 Model screenshot available in `/Dashboard/Executive_Dashboard.png`

---

## 🧠 Features Included

✔ KPI Summary Cards  
✔ Drill-through & Interactive Slicers  
✔ Trend Analysis & Comparative Metrics  
✔ Map Visualizations  
✔ Dynamic DAX Measures  
✔ Time Intelligence Calculations  

---

## 🧮 Key DAX Measures

```DAX
Total Orders = SUM(Orders[OrderCount])

Total Sales = SUM(Orders[TotalSales])

Net Revenue = SUM(Orders[NetRevenue])

Average Order Value = DIVIDE([Total Sales], [Total Orders])

Delivered Orders =
CALCULATE([Total Orders], Orders[OrderStatus] = "Delivered")

On Time Orders =
CALCULATE([Total Orders], Orders[OnTimeFlag] = 1)

Late Deliveries =
CALCULATE(COUNTROWS(Orders), Orders[DeliveryBucket] = "Late")

| Executive Summary        | Sales & Product Analytics | Delivery & Operational Insights |
| ------------------------ | ------------------------- | ------------------------------- |
| ![Executive_Dashboard](Dashboard/Page1.png) | ![Sales_products_Dashboard](Dashboard/Page2.png)  | ![Sales_Products_Dashboard](Dashboard/Page3.png)

| Tool        | Purpose                        |
| ----------- | ------------------------------ |
| Power BI    | Visualization & Reporting      |
| Power Query | Data Cleaning & Transformation |
| DAX         | Measures, KPIs & Logic         |
| Excel       | Primary Data Source            |

📈 Key Insights Derived

🥇 Top performing category: Household

💳 Most used payment method: UPI

🚚 Delivery success rate: 89.50%

⏱ Average delivery time: 27.7 minutes

📅 Best performing month: November 2025  |

🔧 Future Enhancements

🔹 AI Forecasting for future order volume
🔹 Power Automate alerts for late delivery threshold
🔹 Customer segmentation using RFM analysis

👤 Author

Ayush Singh
📊 Data Analyst | Power BI | SQL | Excel

🔗 LinkedIn:www.linkedin.com/in/ayushsh30

⭐ If you like this project, don’t forget to star ⭐ the repository!

