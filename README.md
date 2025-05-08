# ⚡ Global EV Charging Behavior 2024 – SQL Data Analysis Project

This project explores real-world electric vehicle (EV) charging behavior data using SQL. The dataset includes detailed information such as country, city, EV models, manufacturers, charging station types, charging duration, energy delivered, and payment methods. The analysis focuses on uncovering patterns, optimizing insights, and understanding EV charging infrastructure globally.

## 📁 Dataset Overview

**Name:** Global EV Charging Behavior 2024  
**Source Format:** CSV (Imported into MySQL Workbench)  
**Rows:** Multiple thousands (hypothetical large dataset)  
**Columns:**
- Country
- City
- Charging Station
- Charging Station Type
- EV Model
- Manufacturer
- Battery Capacity
- Charging Start Time
- Charging End Time
- Charging Duration
- Energy Delivered
- Charging Cost
- Payment Method
- Temperature
- Charging Session Outcome (Completed, Failed, Aborted)
- Station Utilization Rate

## 🎯 Objectives

- Analyze charging session outcomes across countries.
- Explore EV model distribution by country and manufacturer.
- Identify usage patterns based on energy delivered and cost.
- Surface insights into charging station performance and utilization.
- Practice intermediate-to-advanced SQL concepts.

## 🧠 Concepts Practiced

- `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- `GROUP BY`, `ORDER BY`
- `WHERE`, `LIKE`, `IN`, `NOT LIKE`, `IS NULL`
- `DISTINCT`
- Aliasing (`AS`)
- Basic Arithmetic
- Filtering text and numerical data

## 📊 Key Insights Extracted

- 🔢 **Total charging sessions per country** to measure EV infrastructure usage.
- 🌍 **Top countries where Porsche Taycan & Audi e-tron are most used**.
- ⚡ **Average energy delivered per session per city** to identify top-performing stations.
- 💸 **Charging cost trends and average costs by country**.
- 🔌 **Charging station types with the highest success/failure rates**.
- 🔁 **Session completion vs failure patterns** globally.
- 🔍 **Most used payment methods in different regions**.

## 🧾 Sample Queries

```sql
-- 1. Total charging sessions per country
SELECT Country, COUNT(*) AS total_sessions
FROM ev_charging_data
GROUP BY Country
ORDER BY total_sessions DESC;

-- 2. Top countries for Porsche Taycan & Audi e-tron
SELECT Country, EV_Model, COUNT(*) AS session_count
FROM ev_charging_data
WHERE EV_Model IN ('Porsche Taycan', 'Audi e-tron')
GROUP BY Country, EV_Model
ORDER BY session_count DESC;

-- 3. Average energy delivered per city
SELECT City, ROUND(AVG(Energy_Delivered), 2) AS avg_energy_kWh
FROM ev_charging_data
GROUP BY City
ORDER BY avg_energy_kWh DESC
LIMIT 5;
```

🔎 View more queries in the SQL Queries Folder.

## 🛠️ Tools Used
💻 MySQL Workbench

🗂️ CSV File Import Wizard

📝 SQL Scripting

## 🌐 How to Reproduce
1. Download the dataset: Global EV Charging Behavior 2024.csv

2. Create a new database in MySQL Workbench

3. Define a custom table with appropriate VARCHAR, INT, FLOAT, and DATETIME data types

4. Use the Import Wizard to populate the table from CSV

5. Run the SQL queries provided in this repo

## 📌 Folder Structure
```
ev-charging-sql-project/
├── README.md
├── Global_EV_Charging_2024.csv
├── sql_queries/
│   ├── session_analysis.sql
│   ├── model_distribution.sql
│   └── energy_usage.sql
```
If you found this interesting, let’s connect!

🔗 https://www.linkedin.com/in/ifta-kakazai/

🧠 I'm open to collaboration on SQL/data projects



