# 📊 Sales Analytics Project
This project demonstrates an **end-to-end Data Analytics workflow** using **SQL, Python, Pandas, Numpy, Visualization, and Power BI**.  
The goal is to analyze sales data, clean and process it with Python, query it using SQL, and visualize insights with Power BI dashboards.

---
## 📑 Dataset
**File**: `sales.csv`
**Size**: 1000 rows × 12 columns  

## 🛠 Tools & Technologies
- **SQL** → Aggregations, Joins, Window Functions  
- **Python** → Data cleaning, preprocessing, analysis  
- **Pandas & Numpy** → Data manipulation  
- **Matplotlib & Seaborn** → Visualization  
- **Power BI** → Interactive dashboards & storytelling  
- **GitHub** → Version control & project showcase
- 
## 🔹 SQL Queries
Example queries used in this project:

```sql
-- Total sales per branch
SELECT branch, SUM(total_price) AS total_sales
FROM sales
GROUP BY branch
ORDER BY total_sales DESC;

-- Top 5 products by revenue
SELECT product_name, SUM(total_price) AS revenue
FROM sales
GROUP BY product_name
ORDER BY revenue DESC
LIMIT 5;

-- Profit margin efficiency by city
SELECT city,
       ROUND(SUM(total_price - tax),2) / SUM(total_price) * 100 AS profit_margin
FROM sales
GROUP BY city;
**More queries available in the code**
**## 🚀 Key Insights**
- Branch A generated the highest revenue
- Normal customers contributed more to total sales than Members
- Stationery category contributed to 20% of revenue
- Profit margin efficiency varied significantly across cities

---



## Key Measures (DAX)

```DAX
Total_Sales = SUM(orders[total_price])
Avg_Sales = AVERAGE(orders[total_price])
Reward_Efficiency = DIVIDE(SUM(orders[reward_points]), SUM(orders[total_price]))
 
```
**🔹 Python Analysis**
**Data Cleaning**

-Removed duplicates

-Handled missing values

-Converted datatypes (e.g., date fields)

-Created new columns → profit, profit_margin, points_efficiency

**Exploratory Data Analysis (EDA)** 

-Branch Performance: Total sales per branch & city

-Customer Insights: Spending behavior of Members vs Normal customers

-Product Analysis: Top-selling products and categories

-Reward Efficiency: How reward points relate to sales

**## 🔮 Future Enhancements**
- Add predictive sales forecasting (Prophet / ARIMA in Python)
- Integrate live Power BI Service dashboards
- Automate ETL pipeline


📌 Author

👤 Rithika Jella

📧 Email: rithikajella30@gmail.com

🌐 GitHub:rithika-30

💼 LinkedIn:https://www.linkedin.com/in/rithikajella/
