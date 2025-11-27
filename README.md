# Ferns-and-Petals-Sales-Analysis-EXCEL-project

## 📸 Dashboard Screenshot
![FnP Sales Dashboard](https://github.com/DinakarShetty/Ferns-and-Petals-Sales-Analysis-EXCEL-project/blob/main/FnP%20Sales%20Analysis-Project.png)

---

## 📘 Project Overview
This project is a **Sales Analysis Dashboard** built completely in **Microsoft Excel** using:

- Power Query (ETL & data cleaning)  
- Data Model (Power Pivot)  
- DAX Measures  
- Pivot Tables & Pivot Charts  
- Slicers & Timelines for interactivity  

The dashboard helps analyze **orders, revenue, customer spend and trends** for an online gifting business (FnP).

---

## 🔍 Key Business Questions

1. **Total Revenue:** Identify the overall revenue.
2. **Average Order and Delivery Time:** Evaluate the time taken for orders to be delivered.
3. **Monthly Sales Performance:** Examine how sales fluctuate across the months of 2023.
4. **Top Products by Revenue:** Determine which products are the top revenue generators.
5. **Customer Spending Analysis:** Understand how much customers are spending on
average.
6. **Sales Performance by Top 5 Product:** Track the sales performance of top 5 products.
7. **Top 10 Cities by Number of Orders:** Find out which cities are placing the highest
number of orders.
8. **Order Quantity vs. Delivery Time:** Analyze if higher order quantities impact delivery
times.
9. **Revenue Comparison Between Occasions:** Compare revenue generated across
different occasions.
10. **Product Popularity by Occasion:** Identify which products are most popular during
specific occasions.

---

## 📊 Dashboard Highlights

### **Top KPIs**
- **1000 Total Orders**
- **₹35,20,984 Total Revenue**
- **₹3,520.98 Avg Customer Spent**
- **5.53 Days Avg Order–Delivery Time**

### **Visuals Included**
- Revenue by Occasion  
- Revenue by Category  
- Revenue by Month  
- Revenue by Hour (Order Time)  
- Top 5 Products by Revenue  
- Top 10 Cities by Orders  

### **Filters**
- Order Date (Timeline)
- Delivery Date (Timeline)
- Occasion (Slicer)

---

## 🧱 Data & Modeling

### **1. Power Query**
- Cleaned raw sales data  
- Converted data types  
- Split columns (dates/hours)  
- Added custom columns  

### **2. Data Model**
- Fact Table: **Sales**  
- Dimension Tables: **Date, Product, City, Occasion**  
- Created relationships through Power Pivot  

### **3. DAX Measures**

```DAX
Total Orders = COUNTROWS(Fact_Sales)

Total Revenue = SUM(Fact_Sales[Revenue])

Avg Customer Spent = [Total Revenue] / [Total Orders]

Order Delivery Time = 
AVERAGEX(Fact_Sales, Fact_Sales[Delivery Date] - Fact_Sales[Order Date])
