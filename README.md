# 🌾 Seasonal Agriculture Performance Analysis

## 📌 Project Overview

**Seasonal Agriculture Performance Analysis** is a Data Analytics project that analyzes agricultural performance across different seasons, crops, states, and farming conditions.

The project uses a dataset containing **4,000 farm records and 28 variables** covering crop yield, production, environmental conditions, resource usage, irrigation methods, and economic performance.

The main objective is to identify **seasonal patterns, productivity differences, resource efficiency, profitability trends, environmental relationships, and unusual observations** using data-driven analysis.

---

## 🎯 Problem Statement

Agricultural performance can vary significantly depending on seasonal conditions, farming practices, environmental factors, resource utilization, and market conditions.

Raw agricultural data does not always provide clear insights into these variations.

This project analyzes agricultural data to:

- Compare agricultural performance across **Kharif, Rabi, and Zaid** seasons.
- Identify seasonal patterns and trends.
- Compare crop productivity and profitability.
- Analyze water usage and irrigation efficiency.
- Study relationships between environmental factors and crop yield.
- Examine regional differences in agricultural performance.
- Detect and investigate unusual yield observations.
- Generate data-driven insights and recommendations.

---

## 🎯 Objectives

The major objectives of this project are:

1. Clean and prepare the agricultural dataset.
2. Perform Exploratory Data Analysis (EDA).
3. Analyze seasonal variations in agricultural performance.
4. Compare crop-wise productivity and profitability.
5. Analyze irrigation methods and water efficiency.
6. Study relationships between environmental and agricultural variables.
7. Identify outliers and unusual observations.
8. Compare agricultural performance across states.
9. Generate meaningful insights and recommendations.

---

## 📊 Dataset

The dataset contains:

- **4,000 records**
- **28 variables**
- Multiple crops
- Multiple states and districts
- Kharif, Rabi, and Zaid seasons

### Major Variables

| Category | Variables |
| Farm Information | Farm_ID, State, District, Crop, Season |
| Environmental Factors | Rainfall, Temperature, Humidity, Sunlight |
| Soil Conditions | Soil pH, Soil Moisture, Nitrogen, Phosphorus, Potassium |
| Farming Practices | Irrigation Method, Fertilizer, Pesticide, Seed Quality |
| Productivity | Yield, Production |
| Economic Factors | Market Price, Total Cost, Revenue, Profit |
| Resource Usage | Water Used, Water Efficiency |
| Risk | Disease/Pest Risk |

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

### Analytical Techniques

- Data Cleaning
- Missing Value Treatment
- Duplicate Detection
- Descriptive Statistics
- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis
- Correlation Analysis
- Outlier Detection
- Seasonal Analysis
- Crop-wise Analysis
- Irrigation Efficiency Analysis
- State-wise Analysis

---

## 🧹 Data Cleaning

The dataset was checked for missing values and duplicate records.

### Missing Values Before Cleaning

| Column | Missing Values |
|---|---:|
| Rainfall_mm | 48 |
| Soil_Moisture_pct | 40 |
| Yield_Tonnes_Ha | 32 |

Missing values were treated using group-based median imputation:

- **Rainfall:** Median based on Season
- **Soil Moisture:** Median based on Season
- **Yield:** Median based on Season and Crop

After cleaning:

- Missing values: **0**
- Duplicate records: **0**
- Final dataset: **4,000 × 28**

---

## 📈 Key Analysis Performed

### 1. Seasonal Performance Analysis

The agricultural performance of Kharif, Rabi, and Zaid seasons was compared using:

- Average Yield
- Average Production
- Average Revenue
- Average Profit
- Water Usage
- Water Efficiency

### Seasonal Results

| Season | Avg. Yield (t/ha) | Avg. Production (t) | Avg. Profit (₹) |
|---|---:|---:|---:|
| Kharif | 5.63 | 46.31 | 178,914.65 |
| Rabi | 5.09 | 41.49 | 87,689.47 |
| Zaid | 4.64 | 38.89 | -24,804.82 |

**Key Insight:**  
Kharif showed the strongest overall agricultural performance, while Zaid had the lowest average yield and production and recorded negative average profit.

---

### 2. Crop-wise Profitability Analysis

Crop performance was evaluated using revenue, cost, and profit.

| Crop | Revenue (₹) | Cost (₹) | Profit (₹) |
|---|---:|---:|---:|
| Sugarcane | 1,371,980.11 | 554,792.13 | 817,187.99 |
| Chilli | 1,276,777.23 | 525,898.89 | 750,878.34 |
| Cotton | 639,423.08 | 514,876.17 | 124,546.92 |
| Groundnut | 542,935.50 | 498,077.38 | 44,858.12 |
| Pulses | 528,465.87 | 532,703.92 | -4,238.05 |
| Maize | 457,067.99 | 541,046.32 | -83,978.33 |
| Rice | 423,615.26 | 525,828.76 | -102,213.50 |
| Wheat | 400,104.89 | 523,503.22 | -123,398.34 |

**Key Insight:**  
Sugarcane and Chilli showed the highest average profitability, while Wheat, Rice, and Maize showed negative average profit in this dataset.

---

### 3. Irrigation Method vs Water Efficiency

Water efficiency was compared across irrigation methods.

| Irrigation Method | Water Efficiency |
|---|---:|
| Rainfed | 7.56 |
| Drip | 6.27 |
| Sprinkler | 4.67 |
| Flood | 3.44 |

**Key Insight:**  
Rainfed and Drip categories showed higher average water-efficiency values than Sprinkler and Flood irrigation in this dataset.

> Note: These results show associations within the dataset and should not be interpreted as proof that an irrigation method directly causes higher efficiency.

---

### 4. Correlation Analysis

Important relationships identified through correlation analysis include:

| Variables | Correlation |
|---|---:|
| Yield ↔ Water Efficiency | 0.92 |
| Yield ↔ Production | 0.89 |
| Revenue ↔ Profit | 0.89 |
| Production ↔ Water Efficiency | 0.81 |
| Rainfall ↔ Disease/Pest Risk | 0.63 |
| Yield ↔ Profit | 0.49 |
| Water Used ↔ Yield | 0.39 |
| Rainfall ↔ Yield | 0.03 |

**Key Insight:**  
Yield showed a moderate positive association with Profit and Water Used, while Rainfall had almost no linear relationship with Yield in this dataset.

Some high correlations are expected because certain variables are mathematically or logically related, such as Production and Yield.

---

### 5. Outlier Analysis

The Interquartile Range (IQR) method was used to identify potential outliers in `Yield_Tonnes_Ha`.

- Q1 = **1.05**
- Q3 = **2.84**
- IQR = **1.79**
- Upper Bound = **5.525**
- Potential outliers = **304**

Most potential global outliers were associated with Sugarcane.

The identified unusual observations were investigated rather than automatically removed. This helped avoid removing potentially valid agricultural observations.

---

### 6. State-wise Agricultural Performance

Agricultural performance was compared across states using average yield, production, and profit.

| State | Avg. Yield | Avg. Production | Avg. Profit (₹) |
|---|---:|---:|---:|
| Punjab | 6.12 | 52.23 | 136,025.64 |
| Karnataka | 5.78 | 47.73 | 119,422.34 |
| Gujarat | 5.75 | 48.33 | 117,568.24 |
| Maharashtra | 5.02 | 43.98 | 135,428.86 |
| Telangana | 5.05 | 39.25 | 108,829.62 |
| Tamil Nadu | 4.87 | 40.84 | 117,744.75 |
| Madhya Pradesh | 4.99 | 37.56 | 86,840.76 |
| Andhra Pradesh | 4.63 | 36.91 | 73,453.53 |

**Key Insight:**  
Punjab recorded the highest average yield and production among the analyzed states, while Andhra Pradesh had the lowest average yield, production, and profit.

---

## 💡 Key Findings

The major findings from the analysis are:

- **Kharif** showed the strongest overall agricultural performance.
- **Zaid** recorded the lowest average yield and production.
- Zaid also recorded **negative average profit**.
- Kharif had the highest average water efficiency.
- Sugarcane and Chilli showed the highest profitability.
- Yield had a moderate positive association with Profit.
- Water usage showed a moderate positive association with Yield.
- Irrigation methods showed noticeable differences in average water efficiency.
- Agricultural performance varied significantly across states.
- Several extreme yield observations were detected and investigated.
- Agricultural performance is influenced by multiple interacting factors rather than a single variable.

---

## 📌 Recommendations

Based on the analysis, the following recommendations can be considered:

1. **Improve Zaid-season performance**  
   Investigate environmental and resource factors contributing to lower yield and negative profitability.

2. **Promote efficient water management**  
   Monitor water usage and water efficiency together with crop yield.

3. **Investigate irrigation efficiency**  
   Analyze why some irrigation categories show lower water-efficiency values.

4. **Consider profitability during crop selection**  
   Crop planning should consider revenue, production costs, and expected profit rather than yield alone.

5. **Use region-specific strategies**  
   State-level differences suggest that agricultural planning should consider local environmental and farming conditions.

6. **Use multiple factors for decision-making**  
   Farmers and planners should consider soil, weather, irrigation, crop type, resources, and economic factors together.

---

## 🚀 Future Scope

The project can be further enhanced by:

- Building **Machine Learning models** for yield prediction.
- Developing seasonal profit prediction models.
- Creating an interactive **Power BI dashboard**.
- Integrating real-time weather and rainfall data.
- Adding more detailed soil and farm-management information.
- Developing crop recommendation systems.
- Developing irrigation recommendation systems.
- Using multi-year agricultural data for trend analysis.
- Expanding the dataset to more regions and districts.

The ultimate goal could be to develop a **data-driven agricultural decision-support system**.

---

## ⚠️ Limitations

- The dataset may not represent all agricultural regions or farming conditions.
- Correlation and association do not establish causation.
- Differences between seasons and states may partly reflect differences in crop composition.
- Extreme observations can influence averages and statistical results.
- Some potentially important factors such as labor costs, detailed farm-management practices, and long-term weather patterns are not included.
- Additional real-world and multi-year data would improve the reliability of conclusions.

---

---

# 👩‍💻 Author

**Akanksha Mishra**

📧 Email: akankshamishra2601@gmail.com

💼 LinkedIn: https://www.linkedin.com/in/akankshamishra2601/

---
