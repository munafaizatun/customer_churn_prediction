# SmartChurn: Targeted Discounts for Customer Retention  

## Overview  
Customer churn is a major challenge for utility companies, directly impacting revenue and growth.  

**SmartChurn** uses machine learning to:  
1. Predict which customers are at risk of leaving.  
2. Simulate business interventions (e.g., 20% discount) to measure retention and profitability.  

This project shows how **data science can directly shape business strategy**.  


## Key Results  
- **Model Performance**  
  - Accuracy: ~91%  
  - Precision (churners): ~82%  
  - Recall (churners): ~7% → model misses many true churners  

- **Discount Simulation (20% energy price cut)**  
  - Only ~3% of customers show profit increase under discount  
  - Among churn-prone customers:  
    - 58 → profit increased (+21.7 units)  
    - 63 → profit decreased (−0.05 units)  
  - **Net effect:** small but positive, concentrated in high-risk segments  


## Business Impact  
- Broad discounts are ineffective → lower revenue with little retention gain 
- Targeted discounts work → focus on high churn risk + positive profit impact  
- Discounts can be transformed into a **precision retention strategy**  


Full notebook & analysis: [SmartChurn Project](projects/customer_churn_prediction.html)  
