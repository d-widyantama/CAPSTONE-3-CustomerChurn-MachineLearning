# CAPSTONE-3-CustomerChurn-MachineLearning

# Repository for  Machine Learning application to E-CommerceCustomer Churn

# E-Commerce Customer Churn Prediction with Machine Learning Classification
---
## Context

In the realm of e-commerce, anticipating customer churn is crucial because acquiring new customers incurs substantial costs, potentially offsetting revenue gains.  Where acquiring a new customer is anywhere from **5 to 25 times more expensive** than retaining an existing one. And that’s just one customer!

Accurately predicting customer churn  allows businesses to allocate resources efficiently and enhance overall operational strategies.


To address this challenge, the e-commerce company are building a predictive Machine Learning model to identify customers who are likely to churn.
And devise a strategic plan: 

When the predictive model indicates a customer might churn, the company initiates a loyalty promotion program. This proactive approach not only retains existing customers but also saves the business from the expense of acquiring new ones.


For this case, the policy can be defined as:
- If the model predicts that the customer is churning , the e-commerce will offer a loyalty promotion to other customers.
- If the model predicts that the customer is not churning, the e-commerce will not offer a loyalty promotion to other customers.


## Model Objective

The business will incure higher cost if the model fails to predicts that the customer will not be churning, but it is actually churning.


| |  |
| --- | --- |
If Churn == 1 (Yes), the customer is churning. | **Positive Class**
If Churn == 0 (No), the customer is not churning. | **Negative Class**


Therefore, we would like to identify the potential churning as much as possible, the model should minimize **False Negative** counts and optimize **Recall**, 


we will use **F2 Score** as the primary evaluation metrics for the model.

*beta = 2 (F2-score) : recall twice as important as precision

## Data Profile

The data set belongs to a leading online E-commerce company. The data set contains customer level information and churn status. 

| Column Name | Description |
| --- | --- |
|	Tenure                  | Tenure of a customer in the company.. |
|	WarehouseToHome         | Distance between the warehouse to the customer’s home|
|	NumberOfDeviceRegistered|    Total number of deceives is registered on a particular customer|
|	PreferedOrderCat        |    Preferred order category of a customer in the last month|
|	SatisfactionScore       |   Satisfactory score of a customer on service|
|	MaritalStatus           |   Marital status of a customer|
|	NumberOfAddress         |     Total number of added on a particular customer|
|	Complaint               |   Any complaint has been raised in the last month|
|	DaySinceLastOrder       |   Day since last order by customer|
|	CashbackAmount          |  Average cashback in last month|
|	Churn                   |   Churn flag|


## Outline
1. Data Preparation
2. Model Selection based on F2 Score
    - Logistic Regression
    - Decision Tree
    - KNN 
    - Voting Classifier (Logistic Regression, Decision Tree, KNN)
    - Stacked Model (Logistic Regression, Decision Tree, KNN)
    - Random Forest
    - XGBoost
3. Best Model Tuning and Evaluation
4. Conclusion


## Conclusion
### **Best model for this case is Random Forest Classifier with F2 Score of 0.793**
- The best model is Random Forest Classifier with F2 Score of 0.793
- The model is able to predict the potential churning customers with 79.3% confidence.
- The model is able to reduce the potential loss from customer acquisition cost (CAC) by 57% compared to business as usual.


**Predictive Power:** Leveraging the Random Forest Classifier with an F2 Score of 0.793, we can confidently identify potential churning customers at a 79.3% accuracy rate.

**Financial Impact:** Implementing the predictive model leads to significant cost savings, reducing Customer Acquisition Cost (CAC) by 89.72%. Projected savings amount to Rp 113,241,600.0.

**Strategic Advantage:** The proactive loyalty promotion program not only retains customers but also optimizes resource allocation, ensuring a competitive edge in the e-commerce market.


## Recommendation
### **Leverage proactive approach to retain existing customers**
- Loyalty promotion program should be offered to the customers who are predicted to be churning by the model.
- Focus on actively resolving the customer complaints, as the EDA indicates that the customers who are churning are more likely to have complaints.
- EDA indicates that average cashback values from churning customers are lower than non-churning customers, the company should consider to increase the cashback amount for the churning customers.

### **Apply Machine Learning prediction as the base for customer retention policy**
- The model should be applied to the new customers to predict the potential churning customers.
- The model should be retrained periodically to maintain the model performance.