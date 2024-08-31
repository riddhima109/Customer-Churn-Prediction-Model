# Classification Report

![image](https://github.com/user-attachments/assets/f7703508-37bf-4eff-8221-b4939a576e81)

The classification report provides key metrics to evaluate the performance of the Random Forest classifier, including precision, recall, and f1-score for both classes, along with overall accuracy.

### **Class 0 (Non-Churned Customers)**
- **Precision: 0.82**
  - The precision of 82% indicates that when the Random Forest model predicts a customer will not churn (Class 0), it is correct 82% of the time. This is a strong precision, showing that most of the predicted non-churned customers indeed did not churn.

- **Recall: 0.91**
  - The recall of 91% indicates that the model successfully identified 91% of the actual non-churned customers. This high recall means that the model is very effective at capturing customers who are not at risk of churning.

- **F1-Score: 0.86**
  - The F1-score of 0.86 is the harmonic mean of precision and recall, balancing both metrics to give an overall sense of the model's performance for non-churned customers. This high score reflects the model's strong capability in correctly predicting non-churned customers.

- **Support: 1539**
  - The support of 1539 represents the number of actual non-churned customers in the dataset.

### **Class 1 (Churned Customers)**
- **Precision: 0.66**
  - For customers predicted to churn (Class 1), the precision is 66%. This means that 66% of the customers predicted as churned actually did churn. This indicates a moderate level of confidence in predicting churned customers.

- **Recall: 0.48**
  - The recall of 48% shows that the model correctly identified 48% of the actual churned customers. This lower recall indicates that the model misses more than half of the customers who are actually at risk of churning.

- **F1-Score: 0.56**
  - The F1-score of 0.56 reflects a moderate balance between precision and recall for churned customers. This score indicates that while the model has some ability to predict churned customers, there is room for improvement.

- **Support: 574**
  - The support of 574 represents the number of actual churned customers in the dataset.

### **Overall Model Performance**
- **Accuracy: 0.79**
  - The overall accuracy of 79% means that the Random Forest classifier correctly predicted whether a customer would churn or not 79% of the time. This gives a general sense of the model’s performance but does not account for class imbalances.

- **Macro Average**:
  - **Precision: 0.74**
  - **Recall: 0.70**
  - **F1-Score: 0.71**
  - The macro averages provide a balanced view of the model’s performance across both classes. These averages show that the model performs reasonably well but struggles more with identifying churned customers.

- **Weighted Average**:
  - **Precision: 0.78**
  - **Recall: 0.79**
  - **F1-Score: 0.78**
  - The weighted averages take into account the number of instances in each class. These averages reflect the overall performance of the model, showing that it does well with the majority class (non-churned) but has challenges with the minority class (churned).

# Confusion Matrix:

![image](https://github.com/user-attachments/assets/ee2dbf11-f7b3-49d3-a345-02b318fe0dcd)

The confusion matrix provides a comprehensive view of how the Random Forest model's predictions align with the actual outcomes. It breaks down the model's performance into four key components: True Negatives, False Positives, False Negatives, and True Positives.

1. **True Negatives (TN) = 1,399**
   - **Definition**: These are the customers who **did not churn** (Class 0) and were correctly identified by the model as not churned.
   - **Interpretation**: Out of 1,539 actual non-churned customers, the model correctly predicted 1,399 of them. This indicates a high level of accuracy in identifying customers who are likely to stay.

2. **False Positives (FP) = 140**
   - **Definition**: These are the customers who **did not churn** (Class 0) but were incorrectly predicted by the model as churned.
   - **Interpretation**: The model mistakenly flagged 140 non-churned customers as churned. This could lead to unnecessary retention efforts targeting customers who were not actually at risk of leaving, potentially resulting in inefficient use of resources.

3. **False Negatives (FN) = 297**
   - **Definition**: These are the customers who **did churn** (Class 1) but were incorrectly predicted by the model as not churned.
   - **Interpretation**: The model failed to identify 297 churned customers. This is particularly concerning because these are the customers who were at risk of leaving but were not targeted for retention strategies, potentially leading to revenue loss.

4. **True Positives (TP) = 277**
   - **Definition**: These are the customers who **did churn** (Class 1) and were correctly identified by the model as churned.
   - **Interpretation**: Out of 574 actual churned customers, the model correctly predicted 277 of them. While this shows the model's ability to identify churned customers, there is significant room for improvement to capture more of these at-risk customers.

### **Key Metrics Derived from the Confusion Matrix:**

To further understand the model's performance, let's derive some essential metrics:

1. **Precision (for Class 1 - Churned Customers):**
   \[
   \text{Precision} = \frac{TP}{TP + FP} = \frac{277}{277 + 140} \approx 0.664
   \]
   - **Interpretation**: Approximately 66.4% of the customers predicted as churned were actually churned. This aligns with the precision reported in the classification report (0.66).

2. **Recall (for Class 1 - Churned Customers):**
   \[
   \text{Recall} = \frac{TP}{TP + FN} = \frac{277}{277 + 297} \approx 0.482
   \]
   - **Interpretation**: The model correctly identified about 48.2% of the actual churned customers. This matches the recall reported in the classification report (0.48).

3. **Accuracy:**
   \[
   \text{Accuracy} = \frac{TN + TP}{TN + FP + FN + TP} = \frac{1399 + 277}{1399 + 140 + 297 + 277} \approx 0.799
   \]
   - **Interpretation**: The model correctly predicted churn status for approximately 79.9% of all customers. This is consistent with the accuracy reported in the classification report (0.79).

4. **F1-Score (for Class 1 - Churned Customers):**
   \[
   \text{F1-Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \approx 0.56
   \]
   - **Interpretation**: The F1-score of 0.56 indicates a moderate balance between precision and recall for churned customers, reflecting the overall effectiveness of the model in handling this class.

### **Key Insights:**

1. **High True Negatives (1,399)**:
   - The model is very effective at identifying non-churned customers, which is beneficial for maintaining existing customer relationships without unnecessary interventions.

2. **Moderate True Positives (277)**:
   - While the model does identify some churned customers, capturing only 48.2% of them means that more than half of the at-risk customers are not being targeted for retention efforts. This is a critical area for improvement.

3. **False Positives (140)**:
   - A moderate number of non-churned customers are incorrectly flagged as churned. While not as critical as false negatives, this can still lead to inefficient use of resources in retention strategies.

4. **False Negatives (297)**:
   - The high number of false negatives is concerning, as it represents a significant portion of churned customers who are not being identified by the model. Addressing this should be a priority to reduce potential revenue loss.

# ROC Curve:

![image](https://github.com/user-attachments/assets/39f0d8de-eeeb-40a4-9b4f-77b0c95bfdf6)

The **ROC AUC score of 0.835** for the Random Forest classifier provides insight into its ability to distinguish between churned and non-churned customers. Here's what it means:

**ROC AUC Score: 0.835**

- **Definition**: The ROC AUC (Receiver Operating Characteristic - Area Under the Curve) score measures the model's ability to discriminate between the two classes (churned and non-churned customers) across all possible classification thresholds. The score ranges from 0 to 1:
  - **0.5** indicates no discrimination ability (equivalent to random guessing).
  - **1.0** indicates perfect discrimination.

- **Score of 0.835**: A score of 0.835 indicates that the Random Forest model has a strong ability to distinguish between churned and non-churned customers. This score implies that the model can correctly rank a randomly chosen churned customer higher than a randomly chosen non-churned customer about 83.5% of the time.

### **What This Means:**

- **High Discriminative Ability**: The ROC AUC score of 0.835 suggests that the Random Forest model is quite effective in distinguishing between customers who will churn and those who won't. This strong score reflects the model's capability to make informed predictions, which is crucial for implementing targeted retention strategies.

- **Model Performance**: This score aligns with the overall accuracy and precision metrics observed in the classification report and confusion matrix. The model has a good balance between precision and recall, particularly for the non-churned class, and performs better than a random guess by a significant margin.

- **Practical Implications**: With an ROC AUC score of 0.835, the Random Forest model is reliable for predicting customer churn in most scenarios. It suggests that the model can effectively guide retention efforts, though further tuning might still enhance its performance, especially for identifying churned customers.
