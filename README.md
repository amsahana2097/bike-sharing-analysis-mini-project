# Analyzing Smart City Bike Sharing Data Using Power BI

## 📝 Project Overview
[cite_start]This project explores a comprehensive dataset of bike-sharing systems spanning **25 different cities** with data from **2,855 unique stations**[cite: 3]. [cite_start]By leveraging Power BI, the analysis provides a "snapshot" of the bike-sharing infrastructure to define service reliability and reach[cite: 4, 13].

---

## 🎯 Project Objectives
[cite_start]The primary goal is to analyze the operational efficiency and accessibility of urban bike-sharing networks across multiple international cities[cite: 6]. Specific objectives include:
* [cite_start]**Revenue Analysis**: Identifying which cities generate high and low revenue[cite: 7].
* [cite_start]**Trend Identification**: Finding out how revenue changed over the years[cite: 8].
* [cite_start]**Efficiency Mapping**: Identifying underperforming cities with low cost efficiency[cite: 9].

---

## 🛠️ Data Pre-processing & Modeling
[cite_start]The project utilized **Excel** and **Power BI** to transform raw data into a structured format[cite: 15, 52].

### Data Modeling (Star Schema)
[cite_start]A Fact table and three Dimensional tables were created to organize the data[cite: 16, 17]:
* [cite_start]**STATION_DIM**: Station names and addresses[cite: 18, 41].
* **DATE_DIM**: Breakdown of date and time[cite: 19, 46].
* **CITY_DIM**: City names and codes[cite: 20, 22].

### Key Power BI Transformations
* **Data Cleaning**: Applied `Clean`, `Trim`, and `Capitalize Each Word` functions to the City column[cite: 56].
* **Calculated Columns**:
    * **Availability Ratio**: $Divide([Available Bike], [Bike Stand])$[cite: 59].
    * [cite_start]**Capacity Group**: Categorized stations as **Small** ($\le 20$), **Medium** ($\le 40$), or **Large**[cite: 62, 63].
    * [cite_start]**Station Revenue**: Calculated as $(Fact\_Bike [Bike Stands] - Fact\_Bike[Available Bikes]) \times 3$[cite: 64, 65].
* **Measures**:
    * [cite_start]**Bike Utilization**: $DIVIDE([Total Bike Available], [Total Capacity])$[cite: 70, 71].
    * [cite_start]**Estimated Revenue**: $([total bike stand] - [Total Bike Available]) \times 3$[cite: 74, 75].

---

## 📊 Key Findings & Insights
[cite_start]Analysis of the **57K total bike stands** and **20K available bikes** revealed the following[cite: 259, 260]:

| Metric | Detail |
| :--- | :--- |
| **Top Performers** | [cite_start]**Lund, Dublin, and Bruxelles-Capitale** generate the highest revenue[cite: 261]. |
| **Utilization** | [cite_start]The system operates at an overall bike utilization rate of **0.34 (34%)**[cite: 260]. |
| **Yearly Trend** | [cite_start]Revenue shows a steady and consistent increase from **2022 to 2025**[cite: 267]. |
| **Seasonality** | [cite_start]A significant spike in bike availability occurs in **November**[cite: 264]. |
| **Capacity** | [cite_start]Most stations belong to the **Small** capacity group[cite: 266]. |

---

## 🚀 Recommendations
* **Strategic Expansion**: Cities with higher revenue should consider expanding station capacity or installing additional stations[cite: 282].
* [cite_start]**Resource Optimization**: Stations with consistently low utilization should be recommended for relocation or capacity reduction[cite: 281].
* [cite_start]**Infrastructure Investment**: Cities showing moderate usage may see increased adoption through infrastructure improvements[cite: 280].

---

## 🏁 Conclusion
[cite_start]The bike-sharing system demonstrates steady growth in revenue and strong demand in several major cities[cite: 284]. [cite_start]However, the analysis also reveals uneven utilization across stations, suggesting opportunities to optimize resource allocation through better redistribution strategies and improved infrastructure[cite: 285, 286].
