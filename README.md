
# 🛍️ Ecommerce Data Analysis Project

Welcome to the **Ecommerce Data Analysis Project** – a comprehensive SQL-based analysis designed to uncover actionable insights from real-world retail data.

<div align="center">

🚀 **Prepared by:** [Maham Waseem](https://github.com/Mahamwaseem786)
📧 **Contact:** [mahamwaseem316@gmail.com](mailto:mahamwaseem316@gmail.com)
📁 **Tool Used:** DB Browser for SQLite
📊 **Tech Stack:** SQL, Power Query, SQLite Browser

</div>

---

## 📌 Project Overview

This project focuses on analyzing retail transaction data to derive meaningful business insights. It covers:

* 🔍 **Data Cleaning**
* 🗃️ **Data Categorization**
* 📈 **Statistical Analysis**
* 🌍 **Region-wise Trends**
* ⏰ **Time-based Sales Patterns**

---

## 🧹 Data Cleaning

Performed in **SQLite**, the cleaning phase involved:

✅ Removing missing values and duplicates
✅ Eliminating negative quantities (likely return/refund entries)
✅ Deleting vague or meaningless product descriptions

---

## 🏷️ Product Categorization

* Used SQL queries to categorize products based on the **Description** column.
* Implemented **Power Query** to split and analyze timestamps (date, year, month, time of day).

📌 **Example SQL Snippet:**

```sql
UPDATE Book2 
SET Categories = 'Accessories' 
WHERE Description IN (
  'ANT COPPER L IME BOUDICCA BRACELET',
  'ANT SILVER TURQUOISE BOUDICCA RING',
  'BAROQUE BUTTERFLY EARRINGS PINK',
  ...
);
```

---

## 📊 Statistical & Business Analysis

### 📦 **Transaction Summary**

```sql
SELECT 
  COUNT(*) AS Total_Transactions,
  SUM(Quantity) AS Total_Quantity,
  AVG(Quantity) AS Average_Quantity,
  MAX(Quantity) AS Max_Quantity,
  MIN(Quantity) AS Min_Quantity
FROM Online_Retail;
```

* **Max Quantity Sold:** 80,995
* **Total Transactions:** Calculated with SQL aggregates

---

### 🌎 **Region-Wise Analysis**

```sql
SELECT 
  Country,
  COUNT(*) AS Number_of_Transactions,
  SUM(Quantity) AS Total_Quantity
FROM Online_Retail
GROUP BY Country
ORDER BY Total_Quantity DESC;
```

🔹 **Top Country by Sales:** United Kingdom

---

### 🕒 **Time-Based Sales Trends**

```sql
SELECT 
  TimeWindow,
  COUNT(*) AS Number_of_Transactions,
  SUM(Quantity) AS Total_Quantity
FROM Online_Retail
GROUP BY TimeWindow
ORDER BY Number_of_Transactions DESC;
```

🔹 **Most Active Time Slot:** Afternoon

---

### 🧾 **Category-Wise Insights**

```sql
SELECT 
  Categories,
  COUNT(*) AS Number_of_Transactions,
  SUM(Quantity) AS Total_Quantity
FROM Online_Retail
GROUP BY Categories
ORDER BY Total_Quantity DESC;
```

🔹 **Top-Selling Category:** Home Decor & Accessories

---

## 📁 File Structure

```
📦 Ecommerce_Data_Analysis
 ┣ 📄 README.md
 ┣ 📄 Ecommerce_Data_Analysis_Project.pdf
 ┗ 📂 SQL_Scripts
     ┗ 📜 cleaning_queries.sql
     ┗ 📜 analysis_queries.sql
```

---

## 🏁 Conclusion

This project demonstrates the power of SQL and data cleaning to extract hidden patterns and trends in ecommerce datasets. It enables businesses to make **data-driven decisions** for product strategy, sales timing, and market targeting.


excel dashboard: https://docs.google.com/spreadsheets/d/1wgKrC65wcKhfgpzuukL5Q8Xmzlp1S0f5/edit?usp=sharing&ouid=117436926721799213539&rtpof=true&sd=true

