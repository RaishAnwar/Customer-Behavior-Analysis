# Customer-Behavior-Analysis
End-to-end customer shopping behavior analysis using Python, SQL, and Power BI. Covers data cleaning, EDA, analytical queries, and interactive dashboard insights
# 📊 Data Analytics Project – End-to-End Analysis Using Python, SQL & Power BI

This project demonstrates a complete data analytics workflow, including data loading, cleaning, exploratory data analysis (EDA), SQL-based business insights, interactive Power BI dashboards, and a final analytical report.  
It is designed to showcase practical analytical skills required for Data Analyst / BI Analyst roles.

---

## 🚀 Project Overview
- Load and explore the dataset in **Python**
- Clean and preprocess data (missing values, formatting, feature creation)
- Perform **EDA** to identify patterns and trends
- Run SQL queries in **PostgreSQL / MySQL / SQL Server**
- Build an **interactive Power BI dashboard**
- Create a final **data analysis report** summarizing insights



---

## 🔍 1. Python – Data Loading, Cleaning & EDA

### ✔ Key Tasks Performed
- Imported dataset into **Pandas**
- Handled missing values (mean/median/mode)
- Removed duplicates & corrected data types
- Cleaned inconsistent column names
- Performed exploratory analysis:
  - Summary statistics  
  - Value distributions  
  - Correlation analysis  
  - Outlier detection  

### ✔ Example Python Snippets
python
import pandas as pd

df = pd.read_csv("dataset.csv")

# Handling missing values
df['column'] = df['column'].fillna(df['column'].median())

# Standardizing column names
df.columns = df.columns.str.lower().str.replace(" ", "_")

# Basic EDA
df.info()
df.describe()
df.isnull().sum()


### SQL Analysis (PostgreSQL / MySQL / SQL Server)

SQL was used to answer business questions and perform deeper analysis on cleaned data.

✔ Example Queries

1️⃣ Total Revenue by Category.

SELECT category, SUM(amount) AS total_revenue
FROM sales
GROUP BY category
ORDER BY total_revenue DESC;

2️⃣ Monthly Sales Trend.

SELECT DATE_TRUNC('month', order_date) AS month,
       SUM(amount) AS monthly_sales
FROM sales
GROUP BY month
ORDER BY month;

3️⃣ Top 5 Customers by Spending

SELECT customer_id, SUM(amount) AS total_spent
FROM sales
GROUP BY customer_id
ORDER BY total_spent DESC
LIMIT 5;

4️⃣ Customer Segment Performance
SELECT segment, COUNT(*) AS total_customers, AVG(amount) AS avg_purchase
FROM customers
GROUP BY segment;

3. Power BI Dashboard

An interactive dashboard was created to visualize the most important trends and metrics identified during analysis.

✔ Dashboard Includes

Total revenue, total customers & key KPIs

Category-wise sales & revenue

Time-series trends

Customer behavior by segment

Filters for dynamic exploration





<img width="1397" height="730" alt="cbpower" src="https://github.com/user-attachments/assets/397a8368-3a01-4911-970a-a63131cf3878" />










