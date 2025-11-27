# Ferns-and-Petals-Sales-Analysis-EXCEL-project

## 📸 Dashboard Screenshot
![FnP Sales Dashboard](images/FnP_Sales_Analysis-Project.png)

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

- What is the **total revenue** and **total orders**?
- Which **occasions**, **categories**, months, cities and products generate the most revenue?
- What time of day has highest ordering?
- What is the **average customer spending**?
- How long, on average, does delivery take?

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

### **3. DAX Measures (Examples)**

```DAX
Total Orders = COUNTROWS(Fact_Sales)

Total Revenue = SUM(Fact_Sales[Revenue])

Avg Customer Spent = [Total Revenue] / [Total Orders]

Order Delivery Time = 
AVERAGEX(Fact_Sales, Fact_Sales[Delivery Date] - Fact_Sales[Order Date])
