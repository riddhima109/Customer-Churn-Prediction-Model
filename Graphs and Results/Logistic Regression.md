# Classification Report

              precision    recall  f1-score   support

           0       0.84      0.91      0.88      1539
           1       0.69      0.55      0.61       574

    accuracy                           0.81      2113
   macro avg       0.77      0.73      0.74      2113
weighted avg       0.80      0.81      0.80      2113

This classification report provides a summary of the performance of a Logistic Regression model applied to a customer churn dataset.

### 1. **Precision**
   - **Class 0 (Non-Churners):** Precision is 0.84, meaning that 84% of the customers predicted as non-churners (class 0) were actually non-churners.
   - **Class 1 (Churners):** Precision is 0.69, meaning that 69% of the customers predicted as churners (class 1) were actually churners.

   **Interpretation:** Precision indicates the proportion of true positives (correctly identified churners/non-churners) out of all positive predictions. A higher precision for class 0 suggests that the model is better at correctly identifying non-churners than churners.

### 2. **Recall**
   - **Class 0 (Non-Churners):** Recall is 0.91, meaning that 91% of actual non-churners were correctly identified by the model.
   - **Class 1 (Churners):** Recall is 0.55, meaning that 55% of actual churners were correctly identified.

   **Interpretation:** Recall measures the proportion of actual positives (actual churners/non-churners) that were correctly identified. The high recall for class 0 indicates the model is good at identifying non-churners, but the lower recall for class 1 suggests it misses a significant number of churners.

### 3. **F1-Score**
   - **Class 0 (Non-Churners):** F1-score is 0.88, which is the harmonic mean of precision and recall, balancing both.
   - **Class 1 (Churners):** F1-score is 0.61, indicating a moderate balance between precision and recall.

   **Interpretation:** The F1-score provides a single metric that balances precision and recall, useful when you need to consider both false positives and false negatives. The higher F1-score for class 0 reflects the model's stronger performance in predicting non-churners.

### 4. **Support**
   - **Class 0 (Non-Churners):** There are 1539 instances of non-churners in the dataset.
   - **Class 1 (Churners):** There are 574 instances of churners in the dataset.

   **Interpretation:** Support indicates the number of actual occurrences of each class in the dataset. There are more non-churners than churners, which could influence the model's performance.

### 5. **Accuracy**
   - **Overall accuracy is 0.81 (81%)**, meaning the model correctly predicted churn or non-churn for 81% of the customers.

   **Interpretation:** Accuracy gives the proportion of correctly classified instances out of the total. However, accuracy alone can be misleading if the classes are imbalanced (which they are, in this case).

### 6. **Macro Avg**
   - **Macro avg precision:** 0.77
   - **Macro avg recall:** 0.73
   - **Macro avg F1-score:** 0.74

   **Interpretation:** The macro average calculates the average metric for each class independently, without considering the number of samples in each class. It suggests a moderate overall performance.

### 7. **Weighted Avg**
   - **Weighted avg precision:** 0.80
   - **Weighted avg recall:** 0.81
   - **Weighted avg F1-score:** 0.80

   **Interpretation:** The weighted average takes into account the support (number of true instances) for each class, giving a more balanced overview of the model's performance considering class imbalance. It shows that the model performs reasonably well overall, but with better accuracy and precision in predicting non-churners.



# Confusion Matrix:

![image](https://github.com/user-attachments/assets/78c57fa0-f3fe-4d7e-82b7-5a56ab0bb8ba)

This confusion matrix visualizes the performance of a Logistic Regression model on the customer churn dataset. 

### **Confusion Matrix Overview**
- The confusion matrix is a 2x2 table that compares the actual labels with the model's predictions.
- The matrix is divided into four sections:
  - **True Negatives (TN):** Top-left (0,0) - Non-churners correctly classified as non-churners.
  - **False Positives (FP):** Top-right (0,1) - Non-churners incorrectly classified as churners.
  - **False Negatives (FN):** Bottom-left (1,0) - Churners incorrectly classified as non-churners.
  - **True Positives (TP):** Bottom-right (1,1) - Churners correctly classified as churners.

### **Matrix Values**
- **True Negatives (TN):** 1398 customers who did not churn were correctly identified as non-churners by the model.
- **False Positives (FP):** 141 customers who did not churn were incorrectly identified as churners.
- **False Negatives (FN):** 257 customers who did churn were incorrectly identified as non-churners.
- **True Positives (TP):** 317 customers who did churn were correctly identified as churners.

### **Interpretation**
1. **True Negatives (TN = 1398):** The model is performing well in identifying non-churners, as it correctly classifies a large number of them.
  
2. **False Positives (FP = 141):** There are some non-churners that the model incorrectly predicts as churners. While this is a smaller number compared to the true negatives, it may lead to unnecessary retention efforts on customers who wouldn't have left.

3. **False Negatives (FN = 257):** This is a more critical error, where the model fails to identify customers who are at risk of churning. These missed predictions could result in lost customers that the company might have otherwise retained.

4. **True Positives (TP = 317):** The model correctly identifies a fair number of customers who are at risk of churning, allowing for targeted retention strategies.

# ROC Curve

![image](https://github.com/user-attachments/assets/04ea396a-4266-41d6-b7e3-f24a92d372b2)

The ROC curve presented in the image reflects the performance of a logistic regression model applied to a churn prediction dataset. 

**ROC Curve Analysis:**
The orange line in the graph represents the ROC curve, which is a plot of the True Positive Rate (TPR) against the False Positive Rate (FPR) across various threshold values. This curve visually demonstrates the trade-off between sensitivity (TPR) and the rate of false alarms (FPR) for the logistic regression model as it attempts to classify customers as either churned or not churned.

**AUC (Area Under the Curve):**
The AUC value of 0.86 signifies the model's overall ability to distinguish between customers who will churn and those who will not. AUC values range from 0 to 1, where 0.5 implies random guessing, and 1.0 indicates perfect discrimination. An AUC of 0.86 suggests that the model has a strong ability to correctly classify customers, indicating a high level of accuracy and effectiveness in predicting churn.

**Baseline Comparison:**
The dashed blue line on the ROC plot represents the baseline or reference line, which corresponds to a classifier that makes random guesses. The logistic regression model’s ROC curve being well above this line shows that the model significantly outperforms random chance in predicting customer churn.


The logistic regression model for churn prediction, as indicated by the ROC curve and an AUC of 0.86, demonstrates a high capacity to correctly identify churned versus non-churned customers. This performance metric suggests that the model is reliable and effective in a real-world scenario where predicting customer churn is crucial for business decisions.


### **Overall Model Performance**
- The model performs well in identifying non-churners (TN) but has some difficulty in correctly identifying churners (TP). The higher number of false negatives (FN) suggests that the model might benefit from further tuning or exploring more complex models to better capture the patterns leading to churn.
- The confusion matrix indicates that while the Logistic Regression model is reasonably accurate, it could be improved, especially in terms of recall for the positive class (churners), to reduce the number of false negatives.

