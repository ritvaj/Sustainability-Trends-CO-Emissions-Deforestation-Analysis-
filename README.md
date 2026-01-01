<h1 align="center">Sustainability Trends: Global CO₂ Emissions & Deforestation Analysis</h1>

**A relational SQL + Power BI project exploring global inequalities in emissions and forest loss.**  
The project involved building a MySQL database, cleaning data with Python/Excel, developing metrics, KPIs and creating narrative-rich dashboards in Power BI to cut through misinformation and present clear insights.

---

## Why This Project?
Climate change is often discussed emotionally — some minimize it, others exaggerate it.  
I wanted to apply **business analysis skills** to sustainability data to answer one question:  

*“If data can solve business problems, why can’t it also clarify the truth about climate issues?”*  

This project is my attempt to use **data storytelling** to highlight where responsibility lies and where action is most urgent.  

---

## Objectives
- Analyze global CO₂ emissions and deforestation using World Bank Data.  
- Compare trends across **income groups** and **population levels**.  
- Build dashboards that are **accessible, evidence-backed, and engaging** for both technical and non-technical audiences.  

---

## Tools & Skills Applied
- **SQL (MySQL):** Built relational schema, joins, calculated columns, and PK constraints.  
- **Python (pandas):** Cleaned raw CSV (deforestation).  
- **Excel:** Manual profiling & cleaning for other datasets.  
- **Power BI:** Data model, DAX measures, time intelligence, storytelling visuals.  
- **Accessibility & UX:** High-contrast visuals, simple navigation, alt text, readability focus.  

---

## Repository Structure
- [sql/](sql)  
  - [schema_and_etl.sql](sql/schema_and_etl.sql) → Creates tables and loads data from staging tables.  
  - [analysis_queries.sql](sql/analysis_queries.sql) → Analysis queries used to generate insights for dashboards.  
  - [validation_checks.sql](sql/validation_checks.sql) → Row counts, null checks, and min/max year checks.   
- [python/](python) → Data cleaning scripts (pandas)  
- [dax/](dax) → Core Power BI measures (CO₂ per-capita, population % by income group, forest area loss)
- [data/](data) → Clean datasets (population, income, land area, deforestation, emissions)  
- [docs/](docs) → Project report PDF, schema diagram, and dashboard images 
- [README.md](README.md) → This file  

---

## Process Overview
1. **Extract** — Collected World Bank datasets on emissions, deforestation, population, land area, and income.  
2. **Transform** — Cleaned with Python & Excel; standardized headers, dropped nulls, profiled values.  
3. **Load** — Built a **MySQL relational database** with PKs (`country_code, year`) and merged fact tables.  
4. **Model** — Created a **star schema** with `Dim_Year` and fact tables (`co2_emissions`, `Deforestation`).  
5. **Visualize** — Designed a dual-page Power BI dashboard + 2025 forecast.  

---

# Visuals

### Database Schema
<img src="docs/Relational_model.png" width="700"><br><br>

### Dashboards
**CO₂ Emissions (The Emission Gap)**  
<img src="docs/The_Emission_Gap.jpg" width="700"><br><br>

**Deforestation (Forest Decline)**  
<img src="docs/Forest_Decline.jpg" width="700"><br><br>

**Forest Cover Forecast (2025 & Beyond)**  
<img src="docs/Forest_Cover_Forecast.jpg" width="700"><br><br>

---

## 📊 Key Insights
- **The Emission Gap:**  
  - High/upper-middle income countries are responsible for most of the emissions = **82.2% of global CO₂ emissions** but only **44.5% of the world’s population**.
  - Per capita, Qatar (37.8t) and Bahrain are extreme outliers.  

- **Forest Decline:**  
  - In low and lower-middle income countries, forests are vanishing faster due to reliance on natural resource extraction for economic survival.    
  - Two-thirds of countries have <40% forest cover.
   

- **Forecasting:**  
  - By 2025, tropical nations like Brazil and Indonesia continue downward trends without major reforestation.  
  - Positive turnarounds in Vietnam, Chile, and Türkiye due to strong reforestation policies.  

---

## Visual Design
- Two themed dashboards:  
  - *The Emission Gap* (income vs emissions).  
  - *Forest Decline* (global deforestation risk).  
- Forecast chart with Power BI’s built-in analytics.  
- Accessibility-first: clear labels, high contrast colors, alt text, big-font data labels.  

---

## Lessons Learned
- **ETL matters as much as visuals** — cleaning and consistent schemas saved hours of debugging later.
-  Creating **meaningful tags** from raw parameters can lead to much richer analysis — e.g., in this project, I tagged countries by income per capita into Low / Lower-Middle / Upper-Middle / High income groups to uncover inequality patterns.
- **Storytelling > charts** — recruiters and stakeholders remember narratives, not bar charts.  

---

## How I’d Improve It (Next Iteration) 
- Automate the full ETL pipeline with **Python scripts** instead of manual Excel cleaning.  
- Deploy dashboards to **Power BI Service** for real-time interaction instead of local PBIX.  
- Integrate **cloud SQL (AWS RDS / GCP)** for production-scale datasets.  

---

## References

- [World Bank: Income per capita](https://data.worldbank.org/indicator/NY.ADJ.NNTY.PC.CD)  
- [World Bank: Population](https://data.worldbank.org/indicator/SP.POP.TOTL)  
- [World Bank: Land area](https://data.worldbank.org/indicator/AG.LND.TOTL.K2)  
- [World Bank: Co2 emissions](https://data.worldbank.org/indicator/EN.GHG.CO2.PC.CE.AR5)  
- [World Bank: Deforestation](https://data.worldbank.org/indicator/AG.LND.FRST.ZS) 

--- 

## 👤 About Me
I’m **Ritvaj Madotra**, a data analyst passionate about using **SQL, Python, BI, and storytelling** to drive business impact.  
📌 Connect: [LinkedIn](https://www.linkedin.com/in/ritvajmadotra) | [GitHub](https://github.com/ritvaj)
