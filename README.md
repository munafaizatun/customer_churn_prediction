# SmartChurn: Targeted Discounts for Customer Retention  

## Overview  
Customer churn is a major challenge for utility companies, directly impacting revenue and growth.  

**SmartChurn** uses machine learning to:  
1. Predict which customers are at risk of leaving  
2. Simulate business interventions (e.g., 20% discount) to measure retention and profitability  

This project demonstrates how **data science can directly inform business strategy and optimize revenue.**


## Key Results  
- **Model Performance**  
  - Accuracy: ~91%  
  - Precision (churners): ~81%  
  - Recall (churners): ~6% → model misses many true churners  

- **Discount Simulation (20% energy price cut)**  
  - Only ~2.6% of customers show benefit from the discount
  - Among predicted churners:  
    - 54 → profit increased (+14.85 units) 
    - 60 → profit decreased (−0.04 units)  
  - **Net effect:** small but positive, concentrated among high-risk customers
- **Visual Analysis**
  - **Churn probability shifts slightly downward** for some customers, highlighting targeted retention impact.
  - **Expected profit plot:** most customers unaffected, but a subset of churn-prone customers benefit.
  - **Customer segmentation:** high churn probability + positive ΔProfit → ideal discount targets. 

## Business Impact  
- Broad discounts are ineffective → lower revenue with little retention gain 
- Targeted discounts work → focus on high churn risk + positive profit impact  
- Provides a **precision retention framework**, optimizing resource allocation and maximizing business value  


Full notebook & analysis: [SmartChurn Project](https://github.com/munafaizatun/munafaizatun.github.io/tree/main/projects))  
