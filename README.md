# 🌤 Weather Analysis Dashboard using Live API Data

## 📘 Project Overview
This project — **Weather Analysis Dashboard** — is developed using **Microsoft Power BI**.  
It analyzes **live weather data** fetched through an **API connection**, processes it using **Power Query**, models it with relational tables, and visualizes it through an **interactive dashboard**.  

The report dynamically updates in real time, showing weather metrics like **temperature**, **humidity**, **wind speed**, and **pressure** across multiple cities.

---

## 🎯 Project Objective
The main objective of this project is to:
- Connect Power BI to a **live data API** source.
- Clean, transform, and model the data efficiently.
- Create **interactive visuals** and **dynamic KPIs** that respond to user slicers.
- Provide real-time insights into **weather trends** and **conditions**.

---

## 🔗 Data Source
- **Source Type:** Web API (Live Data)
- **Data Fields:**
  - City / Location Name  
  - Date & Time  
  - Temperature (Current, Min, Max)  
  - Humidity  
  - Wind Speed  
  - Pressure  
  - Visibility  
  - Weather Condition (Sunny, Rainy, Cloudy, etc.)

---

## 🧩 Data Preparation
Performed in **Power Query Editor**:
1. Connected to the live API using Power BI’s Web Connector.  
2. Removed null or unnecessary columns.  
3. **Split nested columns** (e.g., “main.temp” → “Temperature”).  
4. Created multiple tables for Temperature, Wind, Humidity, and Pressure.  
5. Used **Append Queries** to combine similar data from different cities or time intervals.  
6. Built relationships between tables based on **City** and **Date**.

---

## 🗃 Data Modeling
Designed a **Star Schema** model for optimized performance.

**Tables:**
- **FactWeather** → Contains numerical data (Temperature, Humidity, Wind Speed, etc.)
- **DimCity** → City information
- **DimDate** → Date and time details
- **DimCondition** → Weather conditions (Sunny, Rainy, Cloudy)

**Relationships:**
- DimCity → FactWeather (One-to-Many)
- DimDate → FactWeather (One-to-Many)
- DimCondition → FactWeather (One-to-Many)

---

## 🧮 DAX Measures (KPIs)
Created custom DAX measures for dynamic insights:
- `Average Temperature = AVERAGE(FactWeather[Temperature])`
- `Max Temperature = MAX(FactWeather[Temperature])`
- `Min Temperature = MIN(FactWeather[Temperature])`
- `Average Humidity = AVERAGE(FactWeather[Humidity])`
- `Average Wind Speed = AVERAGE(FactWeather[WindSpeed])`
- `Total Cities Covered = DISTINCTCOUNT(DimCity[CityName])`

These KPIs automatically update based on slicer selections.

---

## 📊 Dashboard Visuals
### Key Visual Components:
1. **KPI Cards** — Display current values for temperature, humidity, and wind speed.  
2. **Line Chart** — Shows temperature trends over time.  
3. **Bar / Column Chart** — Compares humidity and pressure across cities.  
4. **Map Visualization** — Displays cities with live weather conditions.  
5. **Slicers** — For filtering data by **City**, **Date**, and **Weather Condition**.  
6. **Dynamic Stickers / Icons** — Weather icons (☀️ 🌧 ☁️) that automatically change based on condition selection.

---

## 📈 Insights
- Identify **temperature trends** over time.  
- Compare **humidity and wind patterns** across locations.  
- Analyze **which cities are hottest or coldest**.  
- Gain **real-time insights** from live API data without manual refresh.  

---

## ⚙️ Key Features
✅ Live API data connection (real-time updates)  
✅ Data transformation using Power Query  
✅ Star schema data modeling  
✅ DAX measures for KPI calculation  
✅ Dynamic visuals and interactive slicers  
✅ Auto-refreshing weather insights  

---

## 🧠 Learnings & Skills Applied
- Power BI (Data Connection, Power Query, DAX, Visualization)
- Data Modeling (Star Schema)
- API Integration for real-time analytics
- Dashboard Design & UX Optimization
- Analytical Thinking & KPI Design

---

## 📂 File Information
**File Name:** `Weather Analysis.pbix`  
**Software Used:** Microsoft Power BI Desktop  
**Version:** Compatible with Power BI Desktop 2024+

---

## 🏁 Conclusion
This project demonstrates the full Power BI workflow — from **connecting to a live API** and **cleaning data**, to **building DAX-driven KPIs** and **interactive dashboards**.  
It provides a **real-time, visually appealing**, and **insightful weather monitoring solution**.  

---

## 🙏 Acknowledgment
Thank you sincerely for reviewing my project.  
It was an excellent learning experience in combining **data integration**, **visual storytelling**, and **real-time analytics** through Power BI.

---

### 👨‍💻 Developed by:
**Aditya Bet**  
Data Scientist | Power BI & Python Enthusiast  
📧 Email: [adityabet214@gmail.com](mailto:adityabet214@gmail.com)  
🔗 GitHub: [https://github.com/adityabet](https://github.com/adityabet)  
🔗 LinkedIn: [https://linkedin.com/in/aditya-bet-592372219](https://linkedin.com/in/aditya-bet-592372219)
