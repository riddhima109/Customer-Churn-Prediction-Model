# Classification report

![image](https://github.com/user-attachments/assets/270d72b6-7c60-4bed-90e5-c4c0f73a869e)

The classification report provides key metrics to evaluate the performance of the SVM model in predicting whether customers will churn. These metrics help us understand how well the model distinguishes between churned and non-churned customers.

### **Class 0 (Non-Churned Customers)**
- **Precision: 0.82**
  - This means that when the SVM model predicts a customer will not churn (Class 0), it is correct 82% of the time. In other words, out of all customers predicted as non-churned, 82% actually did not churn.
  
- **Recall: 0.93**
  - The recall of 93% indicates that the model successfully identified 93% of the customers who truly did not churn. This shows the model is very good at capturing most non-churned customers.
  
- **F1-Score: 0.87**
  - The F1-score combines precision and recall into a single metric. With an F1-score of 0.87, the model shows strong performance in correctly identifying non-churned customers, balancing both the ability to make correct predictions and to find all relevant cases.
  
### **Class 1 (Churned Customers)**
- **Precision: 0.71**
  - For customers predicted to churn (Class 1), the model is correct 71% of the time. This precision indicates that 71% of the customers the model flagged as likely to churn actually did churn.
  
- **Recall: 0.46**
  - The recall of 46% tells us that the model only identified 46% of the customers who actually churned. This lower recall indicates the model misses over half of the churned customers, meaning it struggles to catch all the cases of churn.
  
- **F1-Score: 0.56**
  - The F1-score for churned customers is 0.56, which reflects a moderate balance between precision and recall. It shows that while the model can correctly predict some churned customers, it’s less reliable for this class compared to non-churned customers.

### **Overall Performance**
- **Accuracy: 0.80**
  - The model’s overall accuracy is 80%, meaning it correctly predicts whether a customer will churn or not 80% of the time. While accuracy gives a general sense of performance, it’s important to consider it along with other metrics, especially when dealing with class imbalances (more non-churned than churned customers).
  
- **Macro Average**:
  - **Precision: 0.76, Recall: 0.69, F1-Score: 0.71**
  - These averages treat each class equally, regardless of how many customers are in each class. They indicate the model’s average performance across both churned and non-churned customers.
  
- **Weighted Average**:
  - **Precision: 0.79, Recall: 0.80, F1-Score: 0.79**
  - These averages take into account the number of customers in each class, giving more weight to the non-churned customers since they are more common. This weighted view is often more reflective of overall model performance in imbalanced datasets.

# Confusion Matrix:

![image](https://github.com/user-attachments/assets/1bdde9a4-a8fc-4aae-90a5-4b88e676e7ff)

The confusion matrix provides a detailed breakdown of the SVM model's predictions compared to the actual outcomes. It shows how many predictions were correct and where the model made errors.

1. **True Negatives (TN) = 1430**:
   - These are the customers who did **not churn** (Class 0) and were correctly identified by the model as not churned.
   - Out of 1,539 actual non-churned customers, the model correctly predicted 1,430 of them.

2. **False Positives (FP) = 109**:
   - These are the customers who did **not churn** (Class 0) but were incorrectly predicted by the model as churned.
   - The model mistakenly flagged 109 non-churned customers as churned.

3. **False Negatives (FN) = 311**:
   - These are the customers who **did churn** (Class 1) but were incorrectly predicted by the model as not churned.
   - The model failed to identify 311 churned customers, missing a significant portion of those who actually churned.

4. **True Positives (TP) = 263**:
   - These are the customers who **did churn** (Class 1) and were correctly identified by the model as churned.
   - Out of 574 actual churned customers, the model correctly predicted 263 of them.

### **Key Insights:**

- **True Negatives (1430)** and **True Positives (263)**: These represent the correct predictions where the model successfully identified non-churned and churned customers, respectively.

- **False Positives (109)**: These indicate the instances where the model incorrectly predicted that a customer would churn when they actually didn't. This could lead to unnecessary interventions, like retention efforts aimed at customers who were not at risk of leaving.

- **False Negatives (311)**: These are more concerning because they represent the churned customers that the model failed to identify. Missing these customers means the model is not fully capturing the at-risk customers, which could lead to revenue loss for the business if these customers aren't targeted for retention strategies.


# ROC Curve:

![image](https://github.com/user-attachments/assets/4f412148-1c69-491c-b0f1-3acbccd1b585)

The ROC AUC score of **0.843** provides a measure of the overall performance of the SVM model in distinguishing between churned and non-churned customers. 

### **ROC AUC Score: 0.843**

- **Definition**: The ROC AUC (Receiver Operating Characteristic - Area Under the Curve) score quantifies the model's ability to distinguish between two classes—churned (Class 1) and non-churned (Class 0) in this case. The AUC score ranges from 0 to 1, where:
  - **0.5** indicates no discriminative power (i.e., the model is no better than random guessing).
  - **1.0** indicates perfect discrimination (i.e., the model perfectly separates the two classes).

- **Score of 0.843**: An AUC score of 0.843 suggests that the SVM model performs well in distinguishing between churned and non-churned customers. Specifically, this score indicates that the model has an 84.3% chance of correctly ranking a randomly chosen churned customer higher than a randomly chosen non-churned customer.

### **What This Means:**

- **Strong Discriminative Ability**: A score of 0.843 is considered quite strong, showing that the model has a good ability to differentiate between the two classes. It means the SVM model is generally effective in predicting customer churn versus non-churn with a high degree of accuracy.

- **Model Performance**: This high AUC score complements the findings from the confusion matrix and classification report. While the model shows good overall performance in classifying churned versus non-churned customers, the ROC AUC score indicates it is particularly effective in distinguishing between the classes, even if there are still some areas for improvement, especially in minimizing false negatives.

- **Practical Implications**: In practical terms, an AUC score of 0.843 suggests that the model is useful for applications where accurate prediction of churn is critical. It indicates a robust model that can be effectively used for targeted customer retention strategies, though there's always room for refinement to further enhance its predictive capabilities.

### **Conclusion:**

The ROC AUC score of 0.843 reflects a strong performance of the SVM model in distinguishing between churned and non-churned customers. It indicates that the model is proficient at predicting customer churn, providing a solid foundation for implementing business strategies aimed at improving customer retention.
