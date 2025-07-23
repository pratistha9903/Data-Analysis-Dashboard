
# 📊 Sales Insights Dashboard – Superstore Dataset

## 🔍 Overview
This is a complete data analytics project built using the **Superstore dataset**. It simulates real-world retail data analysis using **Excel**, **SQL**, and **Power BI** to generate actionable business insights.

---

## 🧰 Tools & Technologies
- **Excel** – Data cleaning, profit calculations, pivot tables, basic charts
- **SQLite (SQL)** – Customer analysis, trend extraction, category insights
- **Power BI** – Interactive dashboard with KPIs, filters, and visualizations

---

## 📁 Dataset
- `superstore_cleaned.csv` – Cleaned dataset used in Excel, SQL, and Power BI
- Source: Sample Superstore data (publicly available on Kaggle and Tableau)

---

## ✅ Key Business Insights

| 🔹 Insight Area         | 📌 Insight                                                                 |
|------------------------|--------------------------------------------------------------------------|
| 🗺️ Region-wise Sales     | West region had the highest total sales: ₹7.25 Lakhs                    |
| 💼 Category Profit       | Technology was the most profitable category: ₹1.45 Lakhs                |
| 📦 Top Sub-Categories   | Phones and Chairs contributed the most to sales                         |
| 📈 Sales Trends         | November showed peak monthly sales; Feb had the lowest                  |
| 👥 Customer Segments    | Consumer segment ordered the most items                                 |

---

## 📌 Excel Work
- Cleaned null values and removed duplicates
- Created `Profit %` column using:
=IF(Sales<>0, Profit/Sales * 100, 0)

  ## SQL
   Built Pivot Tables:
- Sales by Region
- Profit by Category
- Monthly Sales Trend
- Top 5 Sub-Categories by Sales
- Visualized using Pivot Charts

---

## 💻 SQL Queries (SQLite)
Some of the key queries used:

```sql
-- Total Sales
SELECT ROUND(SUM(Sales), 2) AS Total_Sales FROM superstore;

-- Profit by Category
SELECT Category, ROUND(SUM(Profit), 2) AS Total_Profit
FROM superstore
GROUP BY Category;

-- Top 5 Customers
SELECT "Customer Name", ROUND(SUM(Sales), 2) AS Total_Sales
FROM superstore
GROUP BY "Customer Name"
ORDER BY Total_Sales DESC
LIMIT 5;

-- Monthly Sales Trend
SELECT SUBSTR("Order Date", 7, 4) || '-' || SUBSTR("Order Date", 4, 2) AS Month,
     ROUND(SUM(Sales), 2) AS Total_Sales
FROM superstore
GROUP BY Month
ORDER BY Month;

```
### 📌 Power BI Dashboard
  - Built interactive report:
  - Cards: Total Sales, Total Profit
  - Bar Charts: Sales by Region, Top Sub-Categories
  - Line Chart: Monthly Sales Trend
  - Filters: Region and Category (Slicers)

---

## 📈 Key Insights

- **Phones** and **Chairs** are top-selling sub-categories
- **Technology** brings in the highest profit
- **Western Region** contributes the most to sales
- **Sales spike** in **November and December**

-----

## 💡 Why This Project?

This project was created to simulate a real business scenario using a public dataset. It demonstrates my skills in:
- Data Cleaning
- SQL Querying
- Dashboard Design
- Insight Communication

---

## 👩‍💻 About Me

**Name:** Pratistha Srivastava  
**Role:** B.Tech CSE (AI/ML), Data Analytics Enthusiast  
**Email:** pratistha9903@gmail.com  
**LinkedIn:** [linkedin.com/in/pratistha9903](https://www.linkedin.com/in/pratistha9903)

---

⭐ *If you liked this project, feel free to star the repo and share your feedback!*
