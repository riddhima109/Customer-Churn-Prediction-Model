# Classification Report:

![image](https://github.com/user-attachments/assets/6d1028d5-19c3-418f-adac-f4b95c03b308)

### **1. Metrics Breakdown**

#### **Precision**
- **Class 0 (No Churn):** 0.80
  - 80% of the instances predicted as no churn were actually no churn.
- **Class 1 (Churn):** 0.58
  - 58% of the instances predicted as churn were actually churn.

#### **Recall**
- **Class 0 (No Churn):** 0.87
  - The model correctly identified 87% of the actual no churn cases.
- **Class 1 (Churn):** 0.45
  - The model correctly identified 45% of the actual churn cases.

#### **F1-Score**
- **Class 0 (No Churn):** 0.84
  - A balanced measure of precision and recall for the no churn class.
- **Class 1 (Churn):** 0.50
  - A balanced measure of precision and recall for the churn class.

#### **Support**
- **Class 0 (No Churn):** 761 instances
  - The number of actual no churn cases in the test set.
- **Class 1 (Churn):** 296 instances
  - The number of actual churn cases in the test set.

### **2. Overall Model Performance**

#### **Accuracy:** 0.75
- The model correctly predicted the churn status of 75% of the instances in the test set.

#### **Macro Average:**
- **Precision:** 0.69
  - The average precision across both classes, treating them equally.
- **Recall:** 0.66
  - The average recall across both classes, treating them equally.
- **F1-Score:** 0.67
  - The average F1-score across both classes, treating them equally.

#### **Weighted Average:**
- **Precision:** 0.74
  - The precision averaged across both classes, weighted by the number of instances in each class.
- **Recall:** 0.75
  - The recall averaged across both classes, weighted by the number of instances in each class.
- **F1-Score:** 0.74
  - The F1-score averaged across both classes, weighted by the number of instances in each class.

### **3. Detailed Interpretation**

#### **Class 0 (No Churn) Performance:**
- **High Recall (0.87):**
  - The model is effective at identifying non-churn cases, with a low false negative rate (only 13% of actual no churn cases were missed).
- **Good Precision (0.80):**
  - When the model predicts no churn, it is correct 80% of the time, although 20% of the no churn predictions are incorrect (some churn cases are misclassified as no churn).

#### **Class 1 (Churn) Performance:**
- **Moderate Precision (0.58):**
  - When the model predicts churn, it is correct 58% of the time, but 42% of the churn predictions are incorrect (some no churn cases are misclassified as churn).
- **Low Recall (0.45):**
  - The model missed 55% of actual churn cases, indicating a high number of false negatives (many churn cases were incorrectly predicted as no churn).

### **4. Overall Insights**

- **Strengths:**
  - The model performs reasonably well in identifying non-churn customers, as indicated by the high recall and F1-score for class 0.
  - The overall accuracy of 75% is acceptable, though there is room for improvement.

- **Weaknesses:**
  - The model struggles to identify churn cases effectively, as shown by the lower recall of 45% and F1-score of 0.50 for class 1.
  - The relatively low precision for churn indicates that the model has a higher rate of false positives for this class, which could lead to unnecessary interventions for customers who were not at risk of churning.

# Confusion Matrix:

![image](https://github.com/user-attachments/assets/a5463e29-09e6-4d1b-985b-5a325354f60b)

### **1. Breakdown of the Confusion Matrix**

- **True Positives (TP):** 132
  - The number of churn cases correctly predicted as churn.

- **True Negatives (TN):** 664
  - The number of non-churn cases correctly predicted as non-churn.

- **False Positives (FP):** 97
  - The number of non-churn cases incorrectly predicted as churn (also known as Type I errors).

- **False Negatives (FN):** 164
  - The number of churn cases incorrectly predicted as non-churn (also known as Type II errors).

### **2. Insights from the Confusion Matrix**

- **Class 0 (No Churn):**
  - **True Negatives (TN):** 664
    - Your model correctly identified 664 out of 761 non-churn cases, which shows a strong ability to detect non-churn customers.
  - **False Positives (FP):** 97
    - However, 97 non-churn cases were incorrectly classified as churn, leading to potential unnecessary customer retention efforts.

- **Class 1 (Churn):**
  - **True Positives (TP):** 132
    - The model correctly identified 132 out of 296 churn cases, which is a significant number but leaves room for improvement.
  - **False Negatives (FN):** 164
    - The model missed 164 churn cases, which is concerning because these are customers who are at risk of leaving but were not identified as such by the model.

### **3. Key Takeaways**

- **Strength in Identifying Non-Churn:**
  - The model is quite effective at identifying non-churn cases, with a relatively low number of false positives.

- **Challenges in Churn Detection:**
  - The model struggles more with accurately identifying churn cases, as indicated by the higher number of false negatives. This means that a significant portion of at-risk customers might not be flagged for intervention.

# Graphs

## Loss Graphs:

![image](https://github.com/user-attachments/assets/0381600a-8bfe-4de3-9b69-322891fdbcd3)

* **Training Loss (Blue Line):**
 - Starts close to 1.0 and decreases sharply within the first 50 epochs, leveling off around 0.5.
 - This indicates that the model quickly learns and improves its performance on the training data.

* **Validation Loss (Orange Line):**
 - Starts just below 1.0 and fluctuates significantly throughout the epochs, ending around 0.7 by epoch 300.
 - The fluctuations suggest variability in the model’s performance on unseen data, and the higher final loss compared to training loss indicates potential overfitting.

* **Trend Analysis:**
 - The rapid decrease in training loss shows effective learning from the training data.
 - The less smooth and higher validation loss suggests that the model may not generalize as well to new data, indicating overfitting.

Overall, the graph shows that while the transformer model learns effectively from the training data, its performance on validation data is less stable and not as strong, suggesting a need for further tuning to improve generalization.

## Accuracy Graphs:

![image](https://github.com/user-attachments/assets/73184967-3f77-4f7d-a182-0402ac9b1c1d)

The graph titled “Accuracy vs Epochs” shows the performance of a transformer model on a churn dataset over 300 epochs. Here’s a detailed interpretation:

* **Training Accuracy (Blue Line):**
 - Starts below 0.1 and increases steadily, reaching close to 0.7 by the end of the graph.
 - This indicates that the model is learning and improving its performance on the training data over time.

* **Validation Accuracy (Orange Line):**
 - Also starts below 0.1 and shows more variability with sharp increases and decreases.
 - Generally trends upwards, fluctuating around 0.6 to just under 0.7 towards the end.
 - The fluctuations suggest variability in the model’s performance on unseen data, but the overall upward trend indicates improvement.

* **Trend Analysis:**
 - Both training and validation accuracies show an initial sharp increase, indicating effective learning in the early epochs.
 - The variability in validation accuracy suggests that the model’s ability to generalize to new data is less stable compared to its performance on training data.

Overall, the graph shows that the transformer model is learning effectively from the training data, but its performance on validation data is less consistent, suggesting a need for further tuning to improve generalization and reduce overfitting.
