# dashboard-task5
# 🚗 Car Sales Dashboard – Power BI

## 📌 Overview
This dashboard was created as part of Task 5 for the Data Analytics Internship. It provides a dynamic, interactive visualization of car sales performance using Power BI, allowing stakeholders to explore key business metrics and trends.

---

## 📁 Dataset Used
A car sales dataset containing:
- `make` (car brand)
- `sellingprice`
- `year`, `state`, `odometer`
- `mmr` (market price), etc.

---

## 📊 Key Features
- **KPI Cards**:
  - Total Cars Sold
  - Average Selling Price
  - Total Revenue
  - Average Odometer Reading

- **Visuals**:
  - Top 10 Brands by Sales Revenue (Bar Chart)
  - Profit Margin % using DAX
  - Dynamic Year-based Title using DAX
  - Slicers for Make, State, and Year

- **Pages**:
  - Page 1: Dynamic Title
  - Page 2: KPIs
  - Page 3: Slicers (filters)
  - Page 4: DAX-based Profit Margin
  - Page 5: Charts and Brand-wise Analysis

---

## 🧠 DAX Used
1. **Profit Margin %**  
```dax
Profit Margin % = 
DIVIDE(
    SUM(car_prices[sellingprice]) - SUM(car_prices[mmr]),
    SUM(car_prices[mmr]),
    0
)
2. Dynamic Title

dax
Copy
Edit
Selected Year Title = 
"Car Sales Dashboard - Year: " & 
IF(
    ISFILTERED(car_prices[year]),
    SELECTEDVALUE(car_prices[year]),
    "All Years"
)
🛠 Tools Used
Microsoft Power BI Desktop

DAX (Data Analysis Expressions)

🎯 Objective
To create a clean, insightful, and interactive sales dashboard using Power BI that allows users to explore business performance across multiple dimensions.
