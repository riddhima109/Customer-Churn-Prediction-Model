# Classification Report

![image](https://github.com/user-attachments/assets/dc5031bf-61e9-4170-ba6b-0a11327a3e45)

The classification report gives key metrics to assess how well the Decision Tree model predicts customer churn. The metrics include precision, recall, and f1-score for each class, along with overall accuracy.

### **Class 0 (Non-Churned Customers)**
- **Precision: 0.82**
  - The precision of 82% indicates that when the Decision Tree model predicts a customer will not churn (Class 0), it is correct 82% of the time. This means that out of all the customers predicted as non-churned, 82% actually did not churn.
  
- **Recall: 0.82**
  - The recall of 82% shows that the model correctly identified 82% of the actual non-churned customers. This indicates that the model is equally effective in identifying non-churned customers as it is precise.
  
- **F1-Score: 0.82**
  - The F1-score of 0.82 is the harmonic mean of precision and recall for non-churned customers. This score suggests that the model performs consistently well in predicting non-churned customers.
  
- **Support: 1539**
  - The support of 1539 represents the number of actual non-churned customers in the dataset.

### **Class 1 (Churned Customers)**
- **Precision: 0.51**
  - For customers predicted to churn (Class 1), the precision is 51%. This means that 51% of the customers predicted as churned actually did churn. The lower precision indicates that the model is less confident in its predictions for churned customers.
  
- **Recall: 0.50**
  - The recall of 50% shows that the model correctly identified half of the actual churned customers. This lower recall means that the model misses a significant portion of churned customers.
  
- **F1-Score: 0.51**
  - The F1-score of 0.51 reflects a moderate balance between precision and recall for churned customers. It indicates that the model's performance in predicting churned customers is not as strong as it is for non-churned customers.
  
- **Support: 574**
  - The support of 574 represents the number of actual churned customers in the dataset.

### **Overall Model Performance**
- **Accuracy: 0.73**
  - The overall accuracy of 73% means that the Decision Tree model correctly predicted whether a customer would churn or not 73% of the time. This gives a general sense of the model’s performance but does not account for class imbalances.
  
- **Macro Average**:
  - **Precision: 0.66**
  - **Recall: 0.66**
  - **F1-Score: 0.66**
  - The macro averages are calculated by taking the average performance across both classes, treating each class equally regardless of its support. These averages provide a balanced view of the model’s performance, showing that it is moderately effective across both classes.

- **Weighted Average**:
  - **Precision: 0.73**
  - **Recall: 0.73**
  - **F1-Score: 0.73**
  - The weighted averages take into account the number of instances in each class. They reflect the model’s overall performance, giving more weight to the non-churned class due to its larger support.

# Confusion Matrix:

![image](https://github.com/user-attachments/assets/245e76a4-46c5-4f4f-9f6d-8dd26f99d222)

The confusion matrix gives a detailed account of how the Decision Tree model’s predictions compare to the actual outcomes. It shows the counts of correct and incorrect predictions for each class.

1. **True Negatives (TN) = 1262**:
   - These are the customers who did **not churn** (Class 0) and were correctly identified by the model as not churned.
   - Out of 1,539 actual non-churned customers, the model correctly predicted 1,262 of them.

2. **False Positives (FP) = 277**:
   - These are the customers who did **not churn** (Class 0) but were incorrectly predicted by the model as churned.
   - The model mistakenly predicted 277 non-churned customers as churned, leading to unnecessary efforts to retain customers who were not at risk.

3. **False Negatives (FN) = 286**:
   - These are the customers who **did churn** (Class 1) but were incorrectly predicted by the model as not churned.
   - The model failed to identify 286 churned customers, which is significant because these are customers who were at risk of leaving but were not correctly targeted for retention strategies.

4. **True Positives (TP) = 288**:
   - These are the customers who **did churn** (Class 1) and were correctly identified by the model as churned.
   - Out of 574 actual churned customers, the model correctly predicted 288 of them.

### **Key Insights:**

- **True Negatives (1262)** and **True Positives (288)**: These represent the correct predictions where the model successfully identified non-churned and churned customers, respectively.

- **False Positives (277)**: These indicate the instances where the model incorrectly predicted that a customer would churn when they actually did not. This could result in wasted resources on retention efforts for customers who were not at risk.

- **False Negatives (286)**: These are particularly concerning because they represent the churned customers that the model failed to identify. Missing these customers could mean losing valuable customers without any intervention.

# ROC Curve

![image](https://github.com/user-attachments/assets/be0de6ee-983b-4152-ab8e-08c8496670b1)

### **ROC AUC Score: 0.661**

- **Definition**: The ROC AUC (Receiver Operating Characteristic - Area Under the Curve) score measures the model's ability to correctly classify churned (Class 1) versus non-churned (Class 0) customers across all possible threshold values. The AUC score ranges from 0 to 1, where:
  - **0.5** suggests no discrimination ability, equivalent to random guessing.
  - **1.0** indicates perfect discrimination, meaning the model perfectly separates the two classes.

- **Score of 0.661**: A score of 0.661 indicates that the Decision Tree model has limited ability to distinguish between churned and non-churned customers. Specifically, this score implies that the model has a 66.1% chance of correctly ranking a randomly chosen churned customer higher than a randomly chosen non-churned customer.

### **What This Means:**

- **Modest Discriminative Ability**: The AUC score of 0.661 suggests that while the model is better than random guessing, its ability to distinguish between the two classes is relatively weak. This low score is consistent with the confusion matrix and classification report, where the model showed challenges in accurately predicting churned customers.

- **Model Performance**: This ROC AUC score complements the findings from the confusion matrix, which revealed a substantial number of False Negatives (missed churned customers) and False Positives (incorrectly identified churned customers). The AUC score reflects the overall uncertainty and potential inaccuracies in the model’s predictions.

- **Practical Implications**: In practical terms, this ROC AUC score means that the Decision Tree model may not be reliable enough for critical churn prediction tasks. The model's limited ability to accurately distinguish between churned and non-churned customers could lead to ineffective retention strategies and missed opportunities for customer intervention.

### **Conclusion:**

The ROC AUC score of 0.661 for the Decision Tree model indicates a modest but underwhelming performance in distinguishing between churned and non-churned customers. This score, along with the other metrics, suggests that while the model has some predictive power, it may not be sufficient for applications where accurate churn prediction is crucial. There might be a need to consider alternative models or further tuning to improve predictive accuracy.
