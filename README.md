# 🌾 Agriculture GCGO Data Analysis Project

> **Grand Challenge & Grand Opportunity | Soil Nutrient Management & Crop Recommendation Analysis**

---

## 📌 Project Overview

This project was developed as part of a data science summative assessment focused on identifying and analysing a **Grand Challenge and Grand Opportunity (GCGO)**. Agriculture was selected as the GCGO due to its central role in African economies and its direct link to recurring food insecurity and famine across the continent.

The analysis uses farm-level soil and crop data to investigate whether fertilizer recommendations are being effectively matched to soil types and crop nutrient requirements — and to propose data-driven solutions that could improve agricultural productivity across Sub-Saharan Africa.

---

## 🎯 Problem Statement

> *African smallholder farmers consistently apply the wrong fertilizers to the wrong soil types, resulting in poor crop yields, wasted resources, and continued food insecurity. This project uses soil characteristics and environmental conditions to identify patterns in nutrient requirements across crop and soil types, and to recommend more targeted fertilizer use.*

---

## 📂 Repository Structure

```
agriculture-gcgo-analysis/
│
├── README.md                        # Project overview (this file)
│
├── data/
│   ├── raw_data.csv                 # Original uncleaned dataset from Kaggle
│   └── clean_data.csv              # Cleaned dataset with derived NPK Total column
│
├── report/
│   └── Agriculture_GCGO_Report.docx  # Full 11-page analysis report
│
└── visuals/
    ├── npk_distribution.png         # Histogram — NPK Total distribution
    ├── npk_by_soil_type.png         # Bar chart — Avg NPK by Soil Type
    ├── nutrients_by_crop.png        # Grouped bar chart — N, P, K by Crop Type
    ├── moisture_vs_npk.png          # Scatter plot — Moisture vs NPK by Soil Type
    └── fertilizer_frequency.png     # Bar/Pie chart — Fertilizer distribution
```

---

## 📊 Dataset

| Attribute | Detail |
|---|---|
| **Source** | [Kaggle — shankarpriya2913](https://www.kaggle.com/datasets/shankarpriya2913/crop-and-soil-dataset) |
| **Rows** | 8,000 unique farm observations |
| **Columns** | 10 (9 original + 1 derived) |
| **Categorical Variables** | Soil Type, Crop Type, Fertilizer Name |
| **Tool Used** | Google Sheets + XLMiner Analysis ToolPak |

### Columns

| Column | Type | Description |
|---|---|---|
| Temperature | Numerical | Ambient temperature at the farm (°C) |
| Humidity | Numerical | Relative humidity (%) |
| Moisture | Numerical | Soil moisture content (%) |
| Soil Type | Categorical | Loamy, Red, Clayey, Sandy, Black |
| Crop Type | Categorical | 11 crop types (Maize, Wheat, Paddy, etc.) |
| Nitrogen (N) | Numerical | Nitrogen content in soil (kg/ha) |
| Potassium (K) | Numerical | Potassium content in soil (kg/ha) |
| Phosphorous (P) | Numerical | Phosphorous content in soil (kg/ha) |
| Fertilizer Name | Categorical | 7 recommended fertilizer types |
| **NPK Total** *(derived)* | Numerical | Sum of N + K + P — total soil nutrient load |

---

## ❓ Seven Analytical Questions

1. What is the distribution of NPK Total levels across the dataset — and what does the spread tell us about overall soil fertility?
2. Which soil type has the highest average NPK Total nutrient load?
3. Is there a statistically significant difference in NPK Total levels across different soil types?
4. Which crop type demands the highest average Nitrogen, Phosphorous, and Potassium levels?
5. Can environmental conditions (Temperature, Humidity, Moisture) predict NPK Total nutrient requirement?
6. What is the relationship between Moisture levels and NPK Total across different soil types?
7. Which fertilizer is most commonly recommended and does it align with the soil types that have the highest nutrient deficits?

---

## 🔍 Analysis Methods Used

| Method | Application |
|---|---|
| Descriptive Statistics | NPK Total distribution, averages by group |
| One-Way ANOVA | Testing NPK differences across soil types |
| Linear Regression | Predicting NPK Total from Temperature, Humidity, Moisture |
| Basic Visualization | Bar charts by soil type and fertilizer |
| Advanced Visualization | Grouped bar chart (N, P, K by crop), scatter plot |

---

## 📈 Key Findings

- **Skewed distribution:** NPK Total is negatively skewed (-0.61), revealing a vulnerable minority of farms with severely depleted soils (below 20 NPK) that are most at risk of crop failure.
- **No significant difference by soil type (ANOVA):** p-value = 0.233 — fertilizer is not being matched to soil type characteristics. A one-size-fits-all approach prevails.
- **Crop-specific nutrient demands:** Millets and Maize demand the most Nitrogen, Oilseeds and Groundnuts need the most Potassium, and Barley and Wheat are the highest Phosphorous consumers.
- **Uniform fertilizer distribution:** All 7 fertilizers are recommended at nearly identical frequencies (13.79%–14.85%), confirming recommendations are not driven by actual soil nutrient levels.
- **Moisture is not a reliable NPK predictor:** No clear relationship exists between soil moisture and NPK Total across soil types.

---

## ✅ Key Recommendations

1. **Soil-type specific fertilizer protocols** — Sandy soils need higher NPK inputs; Clayey soils can sustain lower application rates.
2. **Crop-specific fertilizer guidance** — Cereal crops need phosphorous-rich fertilizers; legumes and oilseeds need potassium-heavy formulations.
3. **Data-driven crop recommendation systems** — Mobile/SMS-based tools that generate tailored fertilizer prescriptions based on soil and crop type.
4. **Targeted intervention for nutrient-poor farms** — Subsidized high-NPK inputs and soil rehabilitation for the most depleted farms.
5. **Soil moisture monitoring infrastructure** — Low-cost sensors to enable precise irrigation and fertilizer timing decisions.

---

## 👥 Stakeholders

| Stakeholder | Role |
|---|---|
| Smallholder Farmers | Primary beneficiaries — apply recommendations on their farms |
| National Governments | Policy development, subsidies, and extension services |
| Agricultural Extension Officers | Train farmers and disseminate soil-specific guidance |
| Fertilizer Companies | Reformulate products to meet crop/soil-specific NPK ratios |
| NGOs & Development Organisations | Fund and implement recommendation systems in rural areas |
| Technology Providers | Build mobile/SMS crop recommendation platforms |
| Research Institutions | Generate soil-specific NPK research for African soil types |

---

## 📚 References

- Food and Agriculture Organization of the United Nations. (2023). *The State of Food Security and Nutrition in the World 2023.* FAO.
- World Bank Group. (2023). *Agriculture and Food.* World Bank.
- African Development Bank Group. (2022). *Feed Africa: Strategy for Agricultural Transformation in Africa 2016–2025.* AfDB.
- Vanlauwe, B., et al. (2014). Sustainable intensification and the African smallholder farmer. *Current Opinion in Environmental Sustainability, 8*, 15–22.
- Tittonell, P., & Giller, K. E. (2013). When yield gaps are poverty traps. *Field Crops Research, 143*, 76–90.

---

## 🛠️ Tools & Technologies

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=flat&logo=google-sheets&logoColor=white)
![XLMiner](https://img.shields.io/badge/XLMiner-Analysis%20ToolPak-blue?style=flat)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?style=flat&logo=github)

---

*This project was completed as part of a Data Science program summative assessment.*
