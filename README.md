Seasonal Agriculture Performance Analysis

VOIS AICTE Batch 1 (2026–2027) — Major Project

Project Overview

This project analyzes farm-level agricultural data to investigate how agricultural performance — yield, production, resource usage, and profitability — varies across the three Indian cropping seasons: Kharif, Rabi, and Zaid. The analysis follows a full data-analytics workflow: dataset inspection, data cleaning, exploratory data analysis, seasonal/environmental/resource/economic analysis, hypothesis testing, and evidence-based recommendations, all documented in a single Jupyter Notebook.

Dataset
File: seasonal_agriculture_performance_dataset.csv
Observations: 4,000 farm records
Variables: 28 columns, covering:
Identifiers/categories: Farm_ID, State, District, Crop, Season, Irrigation_Method
Agricultural/output variables: Farm_Area_Hectares, Yield_Tonnes_Ha, Production_Tonnes, Seed_Quality_Score
Environmental variables: Rainfall_mm, Avg_Temperature_C, Humidity_pct, Sunlight_Hours_Day, Soil_pH, Soil_Moisture_pct, Disease_Pest_Risk_pct
Soil-nutrient variables: Nitrogen_kg_ha, Phosphorus_kg_ha, Potassium_kg_ha
Resource-usage variables: Fertilizer_kg_ha, Pesticide_Litre_ha, Water_Used_m3, Water_Efficiency_t_per_1000m3
Economic variables: Market_Price_INR_Tonne, Total_Cost_INR, Revenue_INR, Profit_INR
Coverage: 8 states, 10 districts, 8 crops, 3 seasons (Kharif, Rabi, Zaid)
Data quality: 0 duplicate rows; missing values found only in Rainfall_mm (48), Soil_Moisture_pct (40), and Yield_Tonnes_Ha (32), which were imputed using season/crop-group medians (see notebook Section 4 for full reasoning).
Objectives
Explore and clean the dataset.
Examine how yield, production, resource usage and profitability vary across seasons.
Investigate relationships between environmental conditions and agricultural outcomes.
Compare resource utilization (water, fertilizer, pesticide) across seasons.
Compare economic performance (revenue, cost, profit) across seasons.
Apply appropriate statistical testing to confirm whether seasonal differences are significant.
Provide evidence-based, data-driven recommendations for seasonal agricultural planning.
Technologies / Libraries Used
Python 3
pandas, numpy — data handling
matplotlib, seaborn — visualization
scipy.stats — hypothesis testing (Shapiro-Wilk, Levene's test, one-way ANOVA, Kruskal-Wallis)
How to Run
Keep Seasonal_Agriculture_Performance_Analysis.ipynb and seasonal_agriculture_performance_dataset.csv in the same folder.
Open the notebook in Jupyter Notebook / JupyterLab / VS Code.
Run all cells in order (Kernel → Restart & Run All). The notebook re-derives every number and chart directly from the CSV, so replacing the CSV with an updated version and re-running will refresh the analysis automatically.
Summary of Analysis

The notebook is organized as a sequential academic report: Introduction → Problem Statement → Objectives → Dataset Description → Data Loading → Data Cleaning → Exploratory Data Analysis → Seasonal Performance Analysis → Environmental Analysis → Resource Analysis → Economic Analysis → Regional/Crop Analysis → Statistical Analysis (hypothesis testing) → Key Findings → Data-Driven Recommendations → Limitations → Conclusion. Every major chart is followed by an Observation / Interpretation / Agricultural Insight discussion grounded in the actual computed values.

Key Findings (from the actual dataset)
Kharif is the strongest season overall, with the highest mean yield (5.64 t/ha), production, water efficiency, and profit (₹178,915 average profit per farm) of the three seasons.
Zaid is the weakest season overall, with the lowest mean yield (4.67 t/ha), lowest water-use efficiency, and a negative average profit (–₹24,805 per farm), despite market prices being nearly identical across all seasons.
Rabi sits in between on nearly every measure (yield: 5.08 t/ha; average profit: ₹87,689).
A Kruskal-Wallis test on crop-adjusted (standardized) yield across the three seasons produced a p-value far below 0.05 — the seasonal difference in performance is statistically significant, not just a visual impression.
The Kharif-strong / Zaid-weak pattern holds broadly across most states and crops, not just in the aggregate.
Rainfall and soil moisture show the strongest positive association with yield among environmental variables — consistent with, but not proof of, a causal water-availability effect.

See the notebook's Key Findings, Recommendations, and Limitations sections for the full, evidence-linked discussion.

Project Structure
.
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Main analysis notebook
├── seasonal_agriculture_performance_dataset.csv      # Source dataset (4,000 rows x 28 cols)
└── README.md                                         # This file
