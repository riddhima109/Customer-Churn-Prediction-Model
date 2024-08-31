# Classification Report

![image](https://github.com/user-attachments/assets/604bac56-8918-418c-8db5-9ba01d276bf1)

The classification report provides important metrics to evaluate how well the KNN model performs in predicting customer churn. The key metrics are precision, recall, and f1-score, which give insight into the model's effectiveness for each class and overall.

### **Class 0 (Non-Churned Customers)**
- **Precision: 0.83**
  - The precision of 83% indicates that when the KNN model predicts a customer will not churn (Class 0), it is correct 83% of the time. This means that out of all the customers predicted as non-churned, 83% actually did not churn.
  
- **Recall: 0.86**
  - The recall of 86% shows that the model correctly identified 86% of the actual non-churned customers. This high recall suggests the model is effective at capturing most of the non-churned customers.
  
- **F1-Score: 0.84**
  - The F1-score of 0.84 is the harmonic mean of precision and recall for non-churned customers. This score reflects a strong balance between precision and recall, indicating good overall performance in predicting non-churned customers.
  
- **Support: 1539**
  - The support of 1539 represents the number of actual non-churned customers in the dataset.

### **Class 1 (Churned Customers)**
- **Precision: 0.58**
  - For customers predicted to churn (Class 1), the precision is 58%. This means that 58% of the customers predicted as churned actually did churn. The lower precision compared to Class 0 suggests that the model makes more mistakes in predicting churned customers.
  
- **Recall: 0.54**
  - The recall of 54% indicates that the model successfully identified 54% of the actual churned customers. This lower recall shows that the model misses a significant portion of churned customers.
  
- **F1-Score: 0.56**
  - The F1-score of 0.56 for churned customers reflects a moderate balance between precision and recall. It shows that while the model can identify some churned customers, its performance is less effective compared to non-churned customers.
  
- **Support: 574**
  - The support of 574 represents the number of actual churned customers in the dataset.

### **Overall Model Performance**
- **Accuracy: 0.77**
  - The overall accuracy of 77% means that the KNN model correctly predicted whether a customer would churn or not 77% of the time. This gives a general sense of the model’s performance but doesn’t account for class imbalances.
  
- **Macro Average**:
  - **Precision: 0.71**
  - **Recall: 0.70**
  - **F1-Score: 0.70**
  - The macro averages are calculated by taking the average performance across both classes, treating each class equally regardless of its support. They provide an overall view of the model’s performance on both classes, with each class having an equal weight in the average.

- **Weighted Average**:
  - **Precision: 0.76**
  - **Recall: 0.77**
  - **F1-Score: 0.77**
  - The weighted averages take into account the number of instances in each class. They provide a performance measure that reflects the proportion of each class in the dataset, giving more weight to the non-churned class due to its larger support.

### **Conclusion:**
The KNN model shows strong performance in identifying non-churned customers, with high precision and recall for this class. However, its performance in predicting churned customers is weaker, as indicated by lower precision, recall, and F1-score for Class 1. This suggests that while the model is effective for predicting non-churned customers, it could benefit from further tuning or additional features to improve its ability to identify churned customers.


# Confusion Matrix:

![image](https://github.com/user-attachments/assets/71f0486c-42ef-4c01-92ed-fcf754de9eae)

The confusion matrix provides a detailed look at how the KNN model’s predictions compare to the actual outcomes. It shows the counts of correct and incorrect predictions for each class.


1. **True Negatives (TN) = 1317**:
   - These are the customers who did **not churn** (Class 0) and were correctly identified by the model as not churned.
   - Out of 1,539 actual non-churned customers, the model correctly predicted 1,317 of them.

2. **False Positives (FP) = 222**:
   - These are the customers who did **not churn** (Class 0) but were incorrectly predicted by the model as churned.
   - The model mistakenly flagged 222 non-churned customers as churned, which could lead to unnecessary retention efforts.

3. **False Negatives (FN) = 265**:
   - These are the customers who **did churn** (Class 1) but were incorrectly predicted by the model as not churned.
   - The model failed to identify 265 churned customers, which could be concerning as these are customers at risk of leaving who were not correctly targeted for retention strategies.

4. **True Positives (TP) = 309**:
   - These are the customers who **did churn** (Class 1) and were correctly identified by the model as churned.
   - Out of 574 actual churned customers, the model correctly predicted 309 of them.

### **Key Insights:**

- **True Negatives (1317)** and **True Positives (309)**: These represent the correct predictions where the model successfully identified non-churned and churned customers, respectively.

- **False Positives (222)**: These indicate the instances where the model incorrectly predicted that a customer would churn when they actually didn't. This could result in unnecessary interventions and retention efforts for customers who were not at risk.

- **False Negatives (265)**: These are particularly critical because they represent the churned customers that the model failed to identify. Missing these customers means that the model is not fully capturing the at-risk customers, potentially leading to missed opportunities for customer retention.

### **Conclusion:**

The confusion matrix shows that the KNN model performs reasonably well in predicting non-churned customers (high True Negatives), but it has a moderate number of False Positives. More importantly, it struggles with identifying churned customers, resulting in a substantial number of False Negatives. While the model is somewhat effective at identifying customers who will stay, its ability to detect customers at risk of churning needs improvement, especially if the goal is to minimize customer loss.

# ROC Curve

![image](https://github.com/user-attachments/assets/72f4cc5a-4a1a-438b-8255-279451c9e597)

### **ROC AUC Score: 0.798**

- **Definition**: The ROC AUC (Receiver Operating Characteristic - Area Under the Curve) score measures the model's ability to discriminate between the two classes—churned (Class 1) and non-churned (Class 0). The AUC score ranges from 0 to 1, where:
  - **0.5** indicates no discriminative power, meaning the model is no better than random guessing.
  - **1.0** indicates perfect discrimination, meaning the model perfectly separates the two classes.

- **Score of 0.798**: An AUC score of 0.798 suggests that the KNN model performs fairly well in distinguishing between churned and non-churned customers. Specifically, this score indicates that the model has about a 79.8% chance of correctly ranking a randomly chosen churned customer higher than a randomly chosen non-churned customer.

### **What This Means:**

- **Good, But Not Outstanding Discriminative Ability**: A score of 0.798 is good, showing that the KNN model has a decent ability to differentiate between the two classes. However, it's not as high as the AUC scores of some other models, suggesting room for improvement.

- **Model Performance**: This AUC score complements the confusion matrix and classification report findings. It shows that while the model performs reasonably well, it’s not as strong in discriminating between churned and non-churned customers as might be desired, especially when compared to more sophisticated models like SVM or logistic regression.

- **Practical Implications**: In practical terms, an AUC score of 0.798 means the KNN model is somewhat reliable for predicting customer churn, but it may miss a considerable number of churned customers or incorrectly flag non-churned customers. This level of performance might still be useful, depending on the context and how critical it is to accurately predict churn.

### **Conclusion:**

The ROC AUC score of 0.798 reflects a decent performance of the KNN model in distinguishing between churned and non-churned customers. While it shows that the model is reasonably effective, it also indicates that there may be better alternatives or further optimization needed to enhance its predictive capabilities, particularly in applications where accurate churn prediction is crucial.

-
