# SmartChurn: Targeted Discounts for Customer Retention

## Project Overview
SmartChurn is a machine learning project that tackles customer churn prediction for a utility company. The goal is not only to predict which customers are likely to leave but also to generate actionable business insights through targeted interventions, such as a 20% discount.

This project mirrors the type of problems solved at BCG X, highlighting the intersection of **data science and business strategy**.  

For more details on the simulation, visit the official BCG Data Science job simulation on The Forage:  
[BCG Data Science Simulation](https://www.theforage.com/simulations/bcg/data-science-ccdz)

## Dataset
- **14,606 customers**, **63 features**
- Key columns:
  - `churn` – target variable indicating customer churn
  - `cons_12m`, `cons_gas_12m` – annual consumption data
  - `forecast_price_energy_*` – predicted energy prices
  - `has_gas` – gas usage indicator
  - `id` – customer identifier

*Source: Proprietary simulated dataset for predictive modeling*

## Data Preparation
- Removed irrelevant columns (`id`, `Unnamed: 0`)
- Separated features (`X`) and target (`y`)
- Encoded categorical variables (`has_gas`)
- Engineered price-related features for discount simulation

**Final dataset:** 61 predictive features across 14,606 customers

## Exploratory Data Analysis (EDA)
EDA focused on understanding:
- Distribution of consumption patterns
- Relationships between pricing and churn
- Data quality and missing values
- Correlations to select predictive features

*Insights from EDA informed feature engineering and model design.*

## Modeling
**Random Forest Classifier** with **Stratified 5-Fold Cross-Validation**:

- Handles nonlinear relationships and noisy data
- Provides interpretable feature importance
- Metrics tracked: Precision, Recall, Accuracy

**Performance Highlights:**
- Overall Accuracy: ~91%
- Recall for churners: ~7% (common in imbalanced datasets)
- Most predictive features: energy consumption, pricing variations, usage history

## Business Impact: Targeted Discounts
To assess actionable interventions, a 20% discount scenario was simulated:

- Calculated expected profit before and after discount:
  `Expected Profit = Probability of Staying × Customer Profit`
- Observed that only ~3% of customers benefit from discounts
- Among predicted churners, targeted discounts increased profit for 58 customers, adding ~21.7 units in total
- Strategic targeting of high-risk churners improves profitability without blanket price reductions

## Conclusion
This project demonstrates a complete **end-to-end machine learning workflow**: data preprocessing, EDA, feature engineering, modeling, evaluation, and business simulation.  

**Impact:** actionable insights for customer retention strategies, showing how predictive analytics can directly inform business decisions.
