# 🌾 Seasonal Agriculture Performance Analysis

### VOIS AICTE Batch 1 (2026–2027) — Major Project

A comprehensive **data analytics project** analyzing farm-level agricultural data to understand how **yield, production, resource utilization, environmental conditions, and profitability** vary across India's three major cropping seasons: **Kharif, Rabi, and Zaid**.

The project follows a complete data analytics workflow, from data inspection and cleaning to exploratory analysis, statistical hypothesis testing, insights, and evidence-based agricultural recommendations.

---

## 📌 Project Overview

Agricultural performance can vary significantly depending on seasonal conditions, environmental factors, resource availability, and economic factors.

This project analyzes **4,000 farm-level records** across **8 states, 10 districts, 8 crops, and 3 cropping seasons** to identify meaningful patterns and determine whether seasonal differences in agricultural performance are statistically significant.

The analysis is implemented entirely in a **Jupyter Notebook**, with every major finding supported by computed statistics and visualizations.

---

## 🎯 Objectives

* Explore and understand the agricultural dataset.
* Clean and preprocess the data appropriately.
* Analyze agricultural performance across Kharif, Rabi, and Zaid seasons.
* Compare seasonal yield and production.
* Investigate relationships between environmental conditions and agricultural outcomes.
* Analyze water, fertilizer, and pesticide utilization.
* Compare revenue, cost, and profitability across seasons.
* Perform statistical hypothesis testing to validate seasonal differences.
* Identify regional and crop-level patterns.
* Develop evidence-based recommendations for seasonal agricultural planning.

---

## 📊 Dataset

**Dataset:** `seasonal_agriculture_performance_dataset.csv`

| Property        | Details            |
| --------------- | ------------------ |
| Total Records   | 4,000              |
| Total Variables | 28                 |
| States          | 8                  |
| Districts       | 10                 |
| Crops           | 8                  |
| Seasons         | Kharif, Rabi, Zaid |
| Duplicate Rows  | 0                  |

### Dataset Variables

#### 🏷️ Identifiers & Categories

* `Farm_ID`
* `State`
* `District`
* `Crop`
* `Season`
* `Irrigation_Method`

#### 🌱 Agricultural & Output Variables

* `Farm_Area_Hectares`
* `Yield_Tonnes_Ha`
* `Production_Tonnes`
* `Seed_Quality_Score`

#### 🌦️ Environmental Variables

* `Rainfall_mm`
* `Avg_Temperature_C`
* `Humidity_pct`
* `Sunlight_Hours_Day`
* `Soil_pH`
* `Soil_Moisture_pct`
* `Disease_Pest_Risk_pct`

#### 🧪 Soil Nutrients

* `Nitrogen_kg_ha`
* `Phosphorus_kg_ha`
* `Potassium_kg_ha`

#### 💧 Resource Usage

* `Fertilizer_kg_ha`
* `Pesticide_Litre_ha`
* `Water_Used_m3`
* `Water_Efficiency_t_per_1000m3`

#### 💰 Economic Variables

* `Market_Price_INR_Tonne`
* `Total_Cost_INR`
* `Revenue_INR`
* `Profit_INR`

---

## 🧹 Data Cleaning

The dataset was inspected for duplicate records, missing values, data types, and consistency issues.

### Missing Values

Missing values were identified only in:

| Column              | Missing Values |
| ------------------- | -------------: |
| `Rainfall_mm`       |             48 |
| `Soil_Moisture_pct` |             40 |
| `Yield_Tonnes_Ha`   |             32 |

These missing values were handled using **season/crop-group median imputation**, preserving the underlying seasonal and crop-level characteristics of the dataset.

### Data Quality

* **0 duplicate rows** were found.
* Missing values were systematically handled.
* Appropriate data types were verified.
* Data was prepared for statistical and visual analysis.

---

## 🔍 Analysis Workflow

The notebook follows a sequential academic data-analysis workflow:

```text
Introduction
     ↓
Problem Statement
     ↓
Objectives
     ↓
Dataset Description
     ↓
Data Loading
     ↓
Data Cleaning & Preprocessing
     ↓
Exploratory Data Analysis
     ↓
Seasonal Performance Analysis
     ↓
Environmental Analysis
     ↓
Resource Analysis
     ↓
Economic Analysis
     ↓
Regional & Crop Analysis
     ↓
Statistical Hypothesis Testing
     ↓
Key Findings
     ↓
Data-Driven Recommendations
     ↓
Limitations
     ↓
Conclusion
```

---

## 📈 Key Findings

### 🥇 Kharif — Strongest Overall Performance

Kharif emerged as the strongest-performing season across several major agricultural indicators.

* **Mean Yield:** 5.64 tonnes/hectare
* **Average Profit:** ₹178,915 per farm
* Highest production performance
* Highest water-use efficiency
* Strong overall agricultural and economic performance

---

### 🥈 Rabi — Intermediate Performance

Rabi generally occupied the middle position between Kharif and Zaid.

* **Mean Yield:** 5.08 tonnes/hectare
* **Average Profit:** ₹87,689 per farm
* Moderate resource efficiency
* Moderate overall agricultural performance

---

### 🥉 Zaid — Weakest Overall Performance

Zaid recorded the weakest performance among the three seasons.

* **Mean Yield:** 4.67 tonnes/hectare
* Lowest water-use efficiency
* **Average Profit:** –₹24,805 per farm
* Negative average profitability despite market prices being nearly identical across seasons

This indicates that lower profitability is primarily associated with differences in production performance and costs rather than major differences in market prices.

---

## 📊 Seasonal Performance Summary

| Metric              |       Kharif |        Rabi |         Zaid |
| ------------------- | -----------: | ----------: | -----------: |
| Mean Yield (t/ha)   |     **5.64** |        5.08 |         4.67 |
| Average Profit/Farm | **₹178,915** |     ₹87,689 | **–₹24,805** |
| Overall Performance |   🥇 Highest | 🥈 Moderate |    🥉 Lowest |

---

## 🧪 Statistical Analysis

Statistical hypothesis testing was performed to determine whether the observed seasonal differences were statistically significant.

The analysis included:

* **Shapiro-Wilk Test** — normality assessment
* **Levene's Test** — variance homogeneity assessment
* **One-Way ANOVA**
* **Kruskal-Wallis Test**

### Kruskal-Wallis Result

A **Kruskal-Wallis test** was performed on crop-adjusted standardized yield across Kharif, Rabi, and Zaid seasons.

The resulting **p-value was far below 0.05**, indicating that the seasonal difference in agricultural performance is **statistically significant**.

Therefore, the observed differences are not simply a result of visual variation in the dataset.

---

## 🌦️ Environmental Analysis

Environmental conditions were analyzed to understand their relationship with agricultural outcomes.

Among the analyzed environmental variables:

* **Rainfall**
* **Soil moisture**

showed the strongest positive association with yield.

This suggests that water availability is an important factor associated with agricultural productivity.

> **Important:** These relationships represent statistical associations and should not be interpreted as proof of causation.

---

## 💧 Resource Utilization Analysis

The project compares seasonal usage and efficiency of:

* Water
* Fertilizer
* Pesticides
* Water-use efficiency

Kharif demonstrated the strongest overall water-use efficiency, while Zaid showed comparatively lower efficiency.

These findings can help identify seasons where better irrigation and resource-management strategies may have the greatest impact.

---

## 💰 Economic Analysis

Economic performance was evaluated using:

* Market price
* Total production cost
* Revenue
* Profit

### Major Finding

Although market prices were nearly identical across the three seasons, profitability varied substantially.

This indicates that **production performance and associated costs** play a major role in determining seasonal profitability.

Kharif generated the highest average profit, while Zaid recorded a negative average profit.

---

## 🌍 Regional & Crop Analysis

The Kharif-strong / Zaid-weak performance pattern was observed broadly across:

* States
* Districts
* Crops

This indicates that the overall seasonal pattern is not limited to a small subset of farms or regions.

---

## 💡 Data-Driven Recommendations

Based on the analysis, the following recommendations can be considered:

### 1. Prioritize Kharif Planning

Kharif demonstrates the strongest combination of yield, resource efficiency, and profitability. Agricultural planning can prioritize high-performing crops and resource allocation during this season.

### 2. Improve Zaid Resource Management

The negative average profitability observed during Zaid highlights the need for improved cost control and resource efficiency.

### 3. Optimize Water Usage

Since rainfall and soil moisture show strong positive associations with yield, efficient irrigation and water-management strategies should receive greater attention, particularly during water-constrained periods.

### 4. Use Crop-Specific Planning

Crop and regional performance differences suggest that agricultural decisions should consider crop-season combinations rather than applying a single strategy to all farms.

### 5. Monitor Environmental Conditions

Tracking rainfall, soil moisture, temperature, and other environmental indicators can support better seasonal planning and resource allocation.

---

## 🛠️ Technologies & Libraries

### Programming Language

* 🐍 Python 3

### Data Analysis

* **Pandas**
* **NumPy**

### Data Visualization

* **Matplotlib**
* **Seaborn**

### Statistical Analysis

* **SciPy**

  * Shapiro-Wilk
  * Levene's Test
  * One-Way ANOVA
  * Kruskal-Wallis Test

### Development Environment

* Jupyter Notebook
* JupyterLab
* VS Code

---

## 📂 Project Structure

```text
Seasonal-Agriculture-Performance-Analysis/
│
├── 📓 Seasonal_Agriculture_Performance_Analysis.ipynb
│   └── Main analysis notebook
│
├── 📊 seasonal_agriculture_performance_dataset.csv
│   └── Source dataset (4,000 rows × 28 columns)
│
└── 📄 README.md
    └── Project documentation
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd Seasonal-Agriculture-Performance-Analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### 4. Open the Notebook

```bash
jupyter notebook
```

Then open:

```text
Seasonal_Agriculture_Performance_Analysis.ipynb
```

### 5. Run the Notebook

Run all cells sequentially:

```text
Kernel → Restart & Run All
```

The notebook derives the analysis, statistics, and visualizations directly from the CSV dataset.

---

## 🔄 Reproducibility

The project is designed to be reproducible.

The notebook does not rely on manually entered results. Numbers, statistical results, and visualizations are generated from the source CSV.

Therefore, replacing the dataset with an updated compatible CSV and rerunning the notebook will automatically refresh the analysis.

---

## ⚠️ Limitations

* The dataset represents a specific sample of farms, states, districts, and crops.
* Statistical associations do not establish causal relationships.
* Seasonal performance may also be influenced by factors not included in the dataset.
* Median imputation was used for missing values, which may introduce some estimation bias.
* Economic outcomes may vary in real-world scenarios due to market fluctuations and external factors.

---

## 🏁 Conclusion

This project demonstrates how data analytics and statistical methods can be used to evaluate agricultural performance across different cropping seasons.

The analysis identifies **Kharif as the strongest-performing season**, while **Zaid shows comparatively weak yield, water efficiency, and profitability**. Environmental factors such as rainfall and soil moisture also show meaningful associations with agricultural yield.

Statistical testing further confirms that the observed seasonal differences are significant.

Overall, the project demonstrates how **data-driven seasonal planning, resource optimization, environmental monitoring, and economic analysis** can support more informed agricultural decision-making.

---

## 👨‍💻 Author

**Pranjal Sharma**

B.Tech — Computer Science Engineering (Artificial Intelligence)
**KIET Group of Institutions**

---

## ⭐ Project Highlights

```text
📊 4,000 Farm Records
🌾 8 Crops
🌍 8 States
📍 10 Districts
☀️ 3 Cropping Seasons
📈 Complete EDA
💧 Resource Efficiency Analysis
💰 Economic Analysis
🧪 Statistical Hypothesis Testing
🤖 Data-Driven Recommendations
```

---

### 📌 Project Type

**Major Project | Data Analytics | Agricultural Analytics | Exploratory Data Analysis | Statistical Analysis | VOIS AICTE Batch 1 (2026–2027)**
