# Customer Churn Prediction & Targeted Discounts

## Overview
Customer churn is a major threat to long-term profitability for utility companies. In this project, I tackled this business challenge by predicting which customers are likely to leave and assessing strategies to retain them using machine learning.

This project is based on the [BCG Data Science job simulation on The Forage](https://www.theforage.com/simulations/bcg/data-science-ccdz), providing a real-world, industry-relevant scenario.

## Problem Statement
High churn rates can significantly impact revenue. The goal was to:

- Predict which customers are at risk of leaving
- Identify key drivers behind churn
- Simulate financial outcomes of targeted interventions, such as a 20% discount

## Dataset
- **14,606 customers**, **63 features**
- Features include consumption patterns, pricing, usage history, and customer attributes
- Target: `churn` (whether the customer leaves)
- Key columns:  
  - `cons_12m`, `cons_gas_12m` – annual consumption  
  - `forecast_price_energy_*` – predicted energy prices  
  - `has_gas` – gas usage indicator  
  - `id` – customer identifier  

## Data Preparation
- Removed irrelevant columns (`id`, `Unnamed: 0`)  
- Separated features (`X`) and target (`y`)  
- Encoded categorical features (`has_gas`)  
- Engineered price-related features to simulate discount scenarios  

Final dataset: **61 predictive features across 14,606 customers**

## Exploratory Data Analysis (EDA)
Through EDA, I explored:

- Consumption patterns across customers  
- Relationships between pricing and churn  
- Data quality, missing values, and initial correlations  

These insights guided feature selection and engineering.

## Modeling
I trained a **Random Forest Classifier** with **Stratified 5-Fold Cross-Validation**:

- Handles nonlinear relationships and noisy data  
- Provides interpretable feature importance  

**Performance Highlights:**

- Overall Accuracy: ~91%  
- Recall for churners: ~7% (common in imbalanced datasets)  
- Top predictive features: energy consumption, pricing variations, usage history

## Business Impact: Targeted Discounts
To simulate actionable interventions, I applied a **20% discount scenario**:

- Expected Profit = Probability of Staying × Customer Profit  
- Only ~3% of customers benefit from discounts  
- Among predicted churners, targeted discounts increase profit for 58 customers (+21.7 units total)  
- Strategic discounting improves profitability without reducing prices for all customers  

## Conclusion
This project demonstrates a complete machine learning workflow: from data preparation and EDA to modeling, evaluation, and business simulation.  

It illustrates how predictive analytics can inform **strategic business decisions**, helping companies retain high-risk customers and improve profitability.
