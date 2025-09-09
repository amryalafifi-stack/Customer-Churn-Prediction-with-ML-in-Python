
## Customer Churn Prediction Project Background


This project analyses customer churn for a mid-sized bank in the financial services industry. The bank has been active for 15 years and operates with a traditional deposit and lending business model. Key metrics include customer retention, churn rate, account balances, and product adoption. 

Provided below is a dashboard containing visuals of all data findings as well as the overview:


<img width="1579" height="730" alt="Screenshot 2025-09-09 at 11 39 35 AM" src="https://github.com/user-attachments/assets/475d52e6-75a2-4d4c-81a0-f85113f8657a" />











Insights and recommendations are provided on the following key areas:

- **Category 1:** Model Performance & Comparison  
- **Category 2:** Customer Segmentation & Risk  
- **Category 3:** Key Drivers of Churn  
- **Category 4:** Churn Prediction Accuracy  

All data processing, analysis, and modeling were conducted using **Python**, including Pandas, Scikit-learn, Matplotlib, and Seaborn.

---

## Data Structure & Initial Checks
The dataset consists of customer-level information including demographic details, account information, transaction summaries, and product adoption metrics.  

Key fields include:

- **Customer ID:** Unique identifier  
- **Age:** Customer age  
- **Estimated Salary:** Annual salary  
- **Credit Score:** Numeric credit rating  
- **Churn:** Target variable (1 = churned, 0 = retained)  

---

## Executive Summary
### Overview of Findings
This analysis reveals that **customer age is the most significant factor influencing churn**, a crucial insight for developing targeted retention campaigns. The **Random Forest model emerged as the most accurate predictive tool** with an AUC of 0.85, outperforming the Logistic Regression model. Using this model, customers can be segmented into distinct risk groups, allowing the business to focus efforts on the most at-risk individuals.  

<img width="1574" height="628" alt="Screenshot 2025-09-09 at 12 46 02 PM" src="https://github.com/user-attachments/assets/2960adf2-122e-4f9d-a4f6-7a4d276fe54a" />






