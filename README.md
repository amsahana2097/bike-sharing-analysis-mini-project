# Analyzing Smart City Bike Sharing Data Using Power BI

## 📝 Project Overview
This project explores a comprehensive dataset of bike-sharing systems spanning **25 different cities** with data from **2,855 unique stations**. By leveraging Power BI, the analysis provides a "snapshot" of the bike-sharing infrastructure to define service reliability and reach.

---

## 🎯 Project Objectives
The primary goal is to analyze the operational efficiency and accessibility of urban bike-sharing networks across multiple international cities. Specific objectives include:
* **Revenue Analysis**: Identifying which cities generate high and low revenue.
* **Trend Identification**: Finding out how revenue changed over the years.
* **Efficiency Mapping**: Identifying underperforming cities with low cost efficiency.

---

## 🛠️ Data Pre-processing & Modeling
The project utilized **Excel** and **Power BI** to transform raw data into a structured format.

### Data Modeling (Star Schema)
A Fact table and three Dimensional tables were created to organize the data:
* **STATION_DIM**: Station names and addresses.
* **DATE_DIM**: Breakdown of date and time.
* **CITY_DIM**: City names and codes.

### Key Power BI Transformations
* **Data Cleaning**: Applied `Clean`, `Trim`, and `Capitalize Each Word` functions to the City column.
* **Calculated Columns**:
    * **Availability Ratio**: $Divide([Available Bike], [Bike Stand])$.
    * **Capacity Group**: Categorized stations as **Small** ($\le 20$), **Medium** ($\le 40$), or **Large**.
    * **Station Revenue**: Calculated as $(Fact\_Bike [Bike Stands] - Fact\_Bike[Available Bikes]) \times 3$.
* **Measures**:
    * **Bike Utilization**: $DIVIDE([Total Bike Available], [Total Capacity])$.
    * **Estimated Revenue**: $([total bike stand] - [Total Bike Available]) \times 3$.

---

## 📊 Key Findings & Insights
Analysis of the **57K total bike stands** and **20K available bikes** revealed the following:

| Metric | Detail |
| :--- | :--- |
| **Top Performers** | **Lund, Dublin, and Bruxelles-Capitale** generate the highest revenue. |
| **Utilization** | The system operates at an overall bike utilization rate of **0.34 (34%)**. |
| **Yearly Trend** | Revenue shows a steady and consistent increase from **2022 to 2025**. |
| **Seasonality** | A significant spike in bike availability occurs in **November**. |
| **Capacity** | Most stations belong to the **Small** capacity group. |

---

## 🚀 Recommendations
* **Strategic Expansion**: Cities with higher revenue should consider expanding station capacity or installing additional stations.
* **Resource Optimization**: Stations with consistently low utilization should be recommended for relocation or capacity reduction.
* **Infrastructure Investment**: Cities showing moderate usage may see increased adoption through infrastructure improvements.

---

## 🏁 Conclusion
The bike-sharing system demonstrates steady growth in revenue and strong demand in several major cities. However, the analysis also reveals uneven utilization across stations, suggesting opportunities to optimize resource allocation through better redistribution strategies and improved infrastructure.
```
