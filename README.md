# SmartChurn: Targeted Discounts for Customer Retention  

## Overview  
Customer churn is a major challenge for utility companies, directly impacting both **revenue stability** and **growth**.  

**SmartChurn** leverages **machine learning** to:  
1. Predict customers most likely to churn.
2. Simulate targeted retention strategies (e.g., 20% price discounts).
3. Quantify financial outcomes to determine when retention efforts are truly profitable.

This project demonstrates how data science can drive business strategy, turning churn prediction into actionable insights for precision-based customer retention.


## Modeling Approach  

- **Algorithm:** Random Forest Classifier (1,000 estimators)  
- **Data:** ~14,600 customers, 61 engineered features  
- **Validation:** 5-fold stratified cross-validation  

| Metric | Score |
|---------|--------|
| Accuracy | ~91% |
| Precision (Churners) | ~81% |
| Recall (Churners) | ~6% |

The model is highly precise, meaning when it predicts a customer is at high churn risk, it’s usually correct — an ideal property for cost-sensitive, targeted retention strategies where false positives are expensive.

## Discount Simulation - 20% Energy Price Cut
To evaluate the financial impact of retention efforts, I simulated a 20% price reduction for high-risk customers and compared churn and profitability outcomes.

| Metric | Result |
|---------|--------|
| Customers benefiting from discount | ~2.6% |
| Predicted churners | 114 |
| Profit increased (churners) | 54 |
| Profit decreased (churners) | 60 |
| **Net profit change** | **+14.85 units** |

**Key Insight:**  
A targeted discount strategy — offering incentives only to high-risk customers — increased overall profit, while broad discounts would have reduced margins.

## Business Impact  
- **Targeted retention works:** Focus incentives on customers with both high churn risk and positive profit contribution.
- **Broad discounts fail:** Blanket offers reduce margins without significantly improving retention.
- **Outcome:** A precision-driven retention framework that optimizes both profitability and customer loyalty.

## Conclusion  

SmartChurn showcases how combining predictive modeling with business simulation can transform raw data into profit-oriented strategy.
By targeting only high-risk customers, companies can achieve higher ROI on retention campaigns while minimizing unnecessary discount costs.
