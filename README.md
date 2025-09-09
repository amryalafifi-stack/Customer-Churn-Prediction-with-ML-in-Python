
## Customer Churn Prediction Project Background


This project analyses customer churn for a mid-sized bank in the financial services industry. The bank has been active for 15 years and operates with a traditional deposit and lending business model. Key metrics include customer retention, churn rate, account balances, and product adoption. 

Provided below is a dashboard containing visuals of all data findings as well as the overview:


<img width="1579" height="730" alt="Screenshot 2025-09-09 at 11 39 35 AM" src="https://github.com/user-attachments/assets/475d52e6-75a2-4d4c-81a0-f85113f8657a" />











Insights and recommendations are provided on the following key areas:

- **Category 1:** Data Structure & Initial Checks  
- **Category 2:** Model Performance & Comparison  
- **Category 3:** Final Assumptions & Recommendations
  
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


### Category 1: Model Performance & Comparison

#### 1. Logistic Regression Model Performance
Logistic Regression is a foundational statistical model used for binary classification problems like predicting churn. It estimates the probability that a customer will churn based on a set of independent variables. The model's performance can be evaluated using a Receiver Operating Characteristic (ROC) curve, which shows how well it can distinguish between churners and non-churners.

In this analysis, the Logistic Regression model served as a benchmark for comparison. It achieved an **AUC of 0.76**, indicating that it performs better than random chance. However, as the ROC curve shows, it is outperformed by the more advanced Random Forest model.  




<img width="539" height="468" alt="Screenshot 2025-09-09 at 9 45 56 AM" src="https://github.com/user-attachments/assets/4ae30b4b-ebb6-453c-9c31-b99a3b35612b" />



---

#### 2. Confusion Matrix - Random Forest
The confusion matrix shows how well the Random Forest model predicts customer churn:

- **True Negatives:** 1,536 (customers correctly predicted to stay)  
- **True Positives:** 185 (customers correctly predicted to churn)  
- **False Positives:** 57 (customers incorrectly predicted to churn)  
- **False Negatives:** 222 (customers incorrectly predicted to stay)  

This indicates that while the model is good at identifying customers who will stay, it struggles more with identifying customers who will leave.  



<img width="528" height="468" alt="Screenshot 2025-09-09 at 9 45 48 AM" src="https://github.com/user-attachments/assets/75c861e6-b946-400a-8730-36edd8ae3de3" />


---

#### 3. Customer Churn Risk Score Distribution
The churn risk score distribution segments customers based on their likelihood to churn. The data shows:

- Majority of customers fall into the **"Safe"** category (low churn risk)  
- Smaller number are on the **"Watchlist"** (moderate risk)  
- A critical, small group is **"High Risk"** (highest probability of churning)  

This segmentation allows the business to efficiently allocate resources, focusing proactive retention efforts on the customers most likely to leave.  



<img width="696" height="472" alt="Screenshot 2025-09-09 at 9 46 06 AM" src="https://github.com/user-attachments/assets/f68d7961-142a-4d56-b75d-101a9c29d69c" />




---

#### 4. Top 10 Features Driving Churn
This bar chart visualizes the factors with the greatest influence on the model's ability to predict churn.  

- **Horizontal bars** show each feature's "importance" score, ranking how much it contributes to the model's predictions.  
- **Key insights:** Age is by far the most important factor, followed by Estimated Salary and Credit Score.  

This insight is critical for creating targeted business strategies, as it shows which aspects of customer data most influence churn outcomes.  


<img width="805" height="470" alt="Screenshot 2025-09-09 at 9 46 16 AM" src="https://github.com/user-attachments/assets/df15091c-61f6-4d53-bf34-bafd52f23b12" />





## Final Assumptions & Recommendations

### Key Drivers & Predictive Insights
Based on the **Random Forest model**, which proved to be the most effective predictive tool for this project, we identified the primary drivers of customer churn:  

- **Age** is by far the most significant factor.  
- **Estimated Salary** and **Credit Score** follow as the next strongest drivers.  

This insight is crucial for targeting specific demographics in retention efforts.  

The model demonstrates strong performance with an **AUC of 0.85**, but the **confusion matrix** highlights a critical limitation:  

- **Correctly identified non-churners (True Negatives):** 1,536  
- **Correctly identified churners (True Positives):** 185  
- **False Positives:** 57  
- **False Negatives:** 222  

This means that while the model is strong at predicting customers who will stay, it struggles to capture a significant portion of those likely to churn.

---

### Recommendations
Based on these insights, the following actions are recommended:

1. **Implement Targeted Retention Campaigns**  
   Since age is the strongest churn driver, marketing and sales teams should develop campaigns tailored to the most at-risk age groups.  

2. **Improve Model Recall**  
   Focus on refining the model to better identify actual churners. Explore alternative algorithms (e.g., Gradient Boosting, XGBoost) or adjust hyperparameters to reduce false negatives.  

3. **Tiered Retention Strategy**  
   Use the churn risk score for segmentation:  
   - **Safe Group:** Light-touch retention monitoring.  
   - **Watchlist:** Automated, proactive interventions.  
   - **High Risk:** Personalised, high-priority outreach.  

---

### Assumptions and Caveats
The following assumptions were made during the analysis:

- **Data Integrity:** It was assumed that the dataset accurately represents customer behaviour.  
- **Model Relevance:** AUC was considered the most important performance metric.  
- **Thresholds:** Risk score cut-offs (Safe <0.3, Watchlist 0.3–0.7, High Risk >0.7) were assumed to be optimal for interventions.  
- **Causality vs. Correlation:** Feature importance values were treated as indicators of causal drivers, though in reality they represent correlation.  



