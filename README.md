# SmartChurn: Targeted Discounts for Customer Retention  

## Project Overview  
SmartChurn is a machine learning project addressing **customer churn prediction** for a utility company.  
The objective is twofold:  
1. **Predict which customers are likely to churn**  
2. **Simulate targeted interventions** (e.g., 20% discount) to evaluate profitability and retention.  

This project mirrors the type of problems solved at **BCG X**, where data science meets **business strategy**.  

Reference: [BCG Data Science Simulation – The Forage](https://www.theforage.com)  



## Dataset  
- **Size:** 14,606 customers  
- **Features:** 63 columns (61 predictive after preprocessing)  
- **Target:** `churn` (1 = churn, 0 = stay)  
- **Key Columns:**  
  - `cons_12m`, `cons_gas_12m` → annual energy/gas consumption  
  - `forecast_price_energy_*` → predicted energy prices  
  - `has_gas` → binary gas usage indicator  
  - `id` → customer identifier  

**Source:** Proprietary simulated dataset for predictive modeling.  



## Data Preparation  
Steps:  
- Dropped irrelevant columns (`id`, `Unnamed: 0`)  
- Encoded categorical variables (`has_gas`)  
- Engineered **price-related features** for discount simulation  
- Split target (`y`) and features (`X`)  

Final dataset: **61 predictive features × 14,606 customers**  



## Exploratory Data Analysis (EDA)  
EDA explored:  
- Distribution of consumption patterns  
- Pricing vs churn relationships  
- Correlations among pricing & contract features  
- Missing values and quality checks  

**Outcome:** Informed feature engineering and model selection.  



## Modeling: Random Forest  
We trained a **Random Forest Classifier** with **5-fold stratified cross-validation**.  

### Why Random Forest?  
- Captures non-linear relationships  
- Robust to noise  
- Provides interpretable feature importance  

**Performance Results:**  
- Accuracy: ~91%  
- Precision (churners): ~82%  
- Recall (churners): ~7% (imbalance issue)  

The model predicts non-churners very well but struggles to detect churners (critical business risk).  

**Key Drivers of Churn:** contract length, pricing features, modification history.  



## Business Simulation: 20% Discount  
We simulated **two scenarios** per customer:  
1. **No Discount** – baseline churn probability & profit  
2. **20% Discount** – energy-related prices reduced by 20% → updated churn probability  

### Key Findings:  
- Only ~3% of customers show profit increase under discount  
- Among predicted churners:  
  - 58 customers → profit increased (+21.7 units total)  
  - 63 customers → profit decreased (−0.05 units)  
- **Net Effect:** +21.7 units extra profit, but **concentrated in a small high-risk segment**  

Discounts are **not universally effective**, but **highly effective when targeted**.  



## Visual Insights  
- **Churn Probability Distribution:** discounts slightly reduce churn risk, but not uniformly.  
- **Expected Profit Comparison:** most customers unchanged, but some churn-prone customers yield higher profit.  
- **Customer Segmentation:**  
  - High churn probability + positive ΔProfit = **ideal discount targets**  
  - Negative ΔProfit = **avoid discounts**  



## Business Impact & Recommendations  
1. **Don’t apply discounts broadly** → wasteful & low ROI  
2. **Targeted retention works**: offer discounts only to churn-prone, profit-positive customers  
3. **Next steps**:  
   - Improve recall (SMOTE, cost-sensitive learning)  
   - Automate discount targeting in production pipeline



## Conclusion  
SmartChurn demonstrates a **complete end-to-end ML workflow**:  
- Data preprocessing  
- EDA & feature engineering  
- Model training & evaluation  
- Business simulation & strategy  

**Impact:** Predictive analytics can directly inform retention strategies — preventing revenue loss while optimizing discount spending.  
