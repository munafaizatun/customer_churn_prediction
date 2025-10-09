# SmartChurn: Targeted Discounts for Customer Retention  

## Overview  
Customer churn is a major challenge for utility companies, directly impacting both **revenue stability** and **growth**.  


**SmartChurn** leverages **machine learning** to:  
1. Predict customers most at risk of churning.  
2. Simulate targeted retention strategies (e.g., 20% discounts).  
3. Quantify financial impact — identifying when retention efforts are profitable.  

This project demonstrates how **data science can directly inform business strategy** and guide **precision retention** decisions.  


## Modeling Approach  

- **Algorithm:** Random Forest Classifier (1,000 estimators)  
- **Data:** ~14,600 customers, 61 engineered features  
- **Validation:** 5-fold stratified cross-validation  

| Metric | Score |
|---------|--------|
| Accuracy | ~91% |
| Precision (Churners) | ~81% |
| Recall (Churners) | ~6% |

The model is highly precise (few false positives), meaning when it flags a customer as high-risk, it’s usually right — ideal for **targeted interventions**.  


## Discount Simulation (20% Energy Price Cut)

Simulated how a **20% price reduction** affects churn and profitability.

| Metric | Result |
|---------|--------|
| Customers benefiting from discount | ~2.6% |
| Predicted churners | 114 |
| Profit increased (churners) | 54 |
| Profit decreased (churners) | 60 |
| **Net profit change** | **+14.85 units** |

**Key Insight:**  
Targeted discounts on high-risk customers can increase profit, while broad discounts erode margins.


## Business Impact  

**Targeted retention works**  
Focus incentives on customers with high churn risk **and** positive profit impact.  

**Broad discounts fail**  
They reduce margins without significantly improving retention.  

**Outcome:**  
A precision-driven customer retention framework — maximizing both **profitability** and **customer loyalty**.


## Conclusion  

SmartChurn proves how **predictive modeling + business simulation** can transform raw data into actionable, profit-driven strategies.  
By targeting only high-risk customers, companies can achieve **higher ROI on retention campaigns** with minimal resource waste.
