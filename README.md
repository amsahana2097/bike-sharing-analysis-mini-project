# Analyzing Smart City Bike Sharing Data Using Power BI

## 📝 Project Overview
[cite_start]This project analyzes a comprehensive dataset of bike-sharing systems across **25 different international cities**[cite: 3]. [cite_start]The data encompasses **2,855 unique stations** [cite: 3][cite_start], capturing a "snapshot" of urban infrastructure to evaluate service reliability, operational efficiency, and accessibility[cite: 4, 6].

---

## 🎯 Objectives
[cite_start]The primary goal is to assess how urban bike-sharing networks perform globally[cite: 6]. Key focus areas include:
* [cite_start]**Revenue Analysis**: Identifying cities with high and low revenue[cite: 7].
* [cite_start]**Temporal Trends**: Tracking how revenue has changed over multiple years[cite: 8].
* [cite_start]**Efficiency**: Pinpointing underperforming cities with low cost-efficiency[cite: 9].
* [cite_start]**Resource Management**: Identifying stations with high capacity but low bike usage[cite: 255].

---

## 🛠️ Data Engineering & Modeling
[cite_start]The project utilized **Excel** and **Power BI** for data preparation and transformation[cite: 15, 52].

### Data Transformation (Power BI)
* [cite_start]**Standardization**: Renamed columns for clarity (e.g., "Contract Name" to "City")[cite: 55].
* [cite_start]**Cleaning**: Applied `Trim`, `Clean`, and `Capitalize Each Word` functions to text data[cite: 56].
* [cite_start]**Parsing**: Split "Date Time" into separate Date and Time columns[cite: 57].

### Calculated Columns & Measures
To drive deeper analysis, the following DAX expressions were implemented:
* [cite_start]**Availability Ratio**: $Divide([Available Bike], [Bike Stand])$ [cite: 59]
* [cite_start]**Capacity Group**: Categorized stations as **Small** ($\le 20$), **Medium** ($\le 40$), or **Large**[cite: 63].
* [cite_start]**Station Revenue**: $(Bike Stands - Available Bikes) \times 3$[cite: 64, 65].
* [cite_start]**Bike Utilization**: $DIVIDE([Total Bike Available], [Total Capacity])$[cite: 71].

---

## 📊 Key Findings & Insights
[cite_start]Analysis of the **57K total bike stands** and **20K available bikes** revealed several critical trends[cite: 259, 260]:

| Metric | Insight |
| :--- | :--- |
| **Top Cities** | [cite_start]**Lund, Dublin, and Bruxelles-Capitale** generate the highest revenue[cite: 261]. |
| **Utilization** | [cite_start]The system operates at an overall bike utilization rate of **0.34 (34%)**[cite: 260]. |
| **Growth** | [cite_start]Yearly revenue shows a steady, consistent increase from **2022 to 2025**[cite: 267]. |
| **Seasonality** | [cite_start]A sharp spike in bike availability occurs in **November**, likely due to winter redistribution[cite: 264, 276]. |

### Capacity Distribution
[cite_start]The majority of stations fall under the **Small** capacity group, with significantly fewer stations categorized as medium or large[cite: 266].

---

## 🚀 Recommendations
Based on the data, the following strategic actions are recommended:
* [cite_start]**Capacity Expansion**: High-revenue cities like Dublin should consider installing additional stations to meet growing demand[cite: 282].
* [cite_start]**Resource Optimization**: Stations with consistently low utilization should be evaluated for relocation or capacity reduction[cite: 281].
* [cite_start]**Infrastructure Investment**: Cities with moderate usage could see increased adoption through promotional initiatives and infrastructure improvements[cite: 280].

---

## 🏁 Conclusion
[cite_start]The bike-sharing system demonstrates steady growth and strong demand in major urban centers[cite: 284]. [cite_start]By implementing better redistribution strategies and expanding high-demand locations, the system can maximize both user satisfaction and revenue generation[cite: 286].
