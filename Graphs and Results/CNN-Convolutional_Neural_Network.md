# Classification Report

![image](https://github.com/user-attachments/assets/7be17677-fab5-4398-9aa8-5984baf5111e)

### **1. Metrics Breakdown**

#### **Precision**
- **Class 0 (No Churn):** 0.83
  - 83% of the instances predicted as no churn were actually no churn.
- **Class 1 (Churn):** 0.69
  - 69% of the instances predicted as churn were actually churn.

#### **Recall**
- **Class 0 (No Churn):** 0.91
  - The model correctly identified 91% of the actual no churn cases.
- **Class 1 (Churn):** 0.51
  - The model correctly identified 51% of the actual churn cases.

#### **F1-Score**
- **Class 0 (No Churn):** 0.87
  - A balanced measure of precision and recall for the no churn class.
- **Class 1 (Churn):** 0.59
  - A balanced measure of precision and recall for the churn class.

#### **Support**
- **Class 0 (No Churn):** 761 instances
  - The number of actual no churn cases in the test set.
- **Class 1 (Churn):** 296 instances
  - The number of actual churn cases in the test set.

### **2. Overall Model Performance**

#### **Accuracy:** 0.80
- The model correctly predicted the churn status of 80% of the instances in the test set.

#### **Macro Average:**
- **Precision:** 0.76
  - The average precision across both classes, treating them equally.
- **Recall:** 0.71
  - The average recall across both classes, treating them equally.
- **F1-Score:** 0.73
  - The average F1-score across both classes, treating them equally.

#### **Weighted Average:**
- **Precision:** 0.79
  - The precision averaged across both classes, weighted by the number of instances in each class.
- **Recall:** 0.80
  - The recall averaged across both classes, weighted by the number of instances in each class.
- **F1-Score:** 0.79
  - The F1-score averaged across both classes, weighted by the number of instances in each class.

### **3. Detailed Interpretation**

#### **Class 0 (No Churn) Performance:**
- **High Recall (0.91):**
  - The model is highly effective at identifying non-churn cases, with only 9% of actual no churn cases being missed (false negatives are low).
- **Good Precision (0.83):**
  - When the model predicts no churn, it is correct 83% of the time, although some churn cases are misclassified as no churn (false positives).

#### **Class 1 (Churn) Performance:**
- **Moderate Recall (0.51):**
  - The model missed 49% of actual churn cases, which indicates a high number of false negatives (churn cases predicted as no churn).
- **Moderate Precision (0.69):**
  - When the model predicts churn, it is correct 69% of the time, but 31% of the churn predictions are incorrect (no churn cases misclassified as churn).

### **4. Overall Insights**

- **Strengths:**
  - The model is strong in identifying no churn cases, which is reflected in the high recall and F1-score for class 0.
  - The accuracy of 80% is solid, indicating a generally well-performing model.

- **Weaknesses:**
  - The model struggles with identifying churn cases, as shown by the relatively low recall of 51% for class 1. This indicates that many churn cases are being missed, which can be a critical issue in churn prediction tasks.

### **Conclusion**

This classification report highlights that while your CNN model is strong in identifying non-churn customers, it has room for improvement in detecting churn cases. By focusing on enhancing the recall for the churn class, you can improve the model's effectiveness in identifying customers at risk of leaving. This will be crucial for making more informed decisions in churn management and customer retention strategies.


# Confusion Matrix:

![image](https://github.com/user-attachments/assets/7cb56d79-630a-4b21-ac17-9fae9f837b46)

The confusion matrix provides a breakdown of your model’s performance in terms of true positives, true negatives, false positives, and false negatives.

#### **1. True Negatives (TN): 693**
- These are the instances where the model correctly predicted **no churn**.
- **693 out of 761** actual no churn cases were correctly identified.

#### **2. False Positives (FP): 68**
- These are the instances where the model incorrectly predicted **churn** when the actual class was no churn.
- **68 out of 761** actual no churn cases were incorrectly classified as churn.

#### **3. False Negatives (FN): 144**
- These are the instances where the model incorrectly predicted **no churn** when the actual class was churn.
- **144 out of 296** actual churn cases were incorrectly classified as no churn.

#### **4. True Positives (TP): 152**
- These are the instances where the model correctly predicted **churn**.
- **152 out of 296** actual churn cases were correctly identified.

### **Detailed Interpretation**

#### **Class 0 (No Churn) Performance:**
- **True Negatives (693):**
  - The model is highly effective at identifying non-churn cases, with a high number of correct predictions.
- **False Positives (68):**
  - There is a relatively small number of non-churn cases that were incorrectly classified as churn. These false positives may lead to unnecessary retention efforts for customers who were not at risk of churning.

#### **Class 1 (Churn) Performance:**
- **True Positives (152):**
  - The model successfully identified 152 churn cases, which is critical for taking proactive retention measures.
- **False Negatives (144):**
  - The model missed 144 actual churn cases, which is concerning because these customers were incorrectly predicted as non-churn and may leave without intervention.

### **Overall Implications**

- **Strengths:**
  - The model continues to perform well in identifying non-churn customers, with a high number of true negatives.
  - The precision for non-churn remains strong, indicating that the model is reliable when it predicts a customer will not churn.

- **Weaknesses:**
  - The model has a significant number of false negatives, meaning it struggles to correctly identify churn cases.
  - This indicates that the model’s recall for the churn class is not optimal, and many churn cases are going undetected.

# Graphs
## Loss Graph:

![image](https://github.com/user-attachments/assets/14219b18-3ef6-4ca1-87d0-562fcab6c9f3)

The graph titled “Loss vs Epochs” shows the performance of a Convolutional Neural Network (CNN) model on a churn dataset over 20 epochs. Here’s a detailed interpretation:

* **Training Loss (Blue Line):**
 - Starts at around 0.65 and steadily decreases to about 0.40 by epoch 20.
 - This indicates that the model is learning and improving its performance on the training data over time.

* **Validation Loss (Orange Line):**
 - Begins just below 0.60 and decreases to approximately 0.45 by epoch 20.
 - The validation loss is consistently higher than the training loss, which suggests that the model performs better on the training data compared to the validation data.

* **Trend Analysis:**
 - Both training and validation losses show a downward trend, indicating overall improvement in model performance.
 - The gap between training and validation losses after around epoch 5 suggests some degree of overfitting, where the model is fitting the training data better than the unseen validation data.

Overall, the graph shows that the model is learning effectively, but the difference between training and validation losses indicates that further tuning might be needed to improve generalization and reduce overfitting.

## Accuracy Graphs:

![image](https://github.com/user-attachments/assets/014a389e-e3c1-4e93-9ee7-be395b3e9711)

* **Training Accuracy (Blue Line):**
 - Starts at around 0.72 and increases sharply until about epoch 5, after which it continues to rise more gradually.
 - Plateaus near epoch 15, reaching an accuracy of approximately 0.82.
 - This indicates that the model is learning and improving its performance on the training data over time.

* **Validation Accuracy (Orange Line):**
 - Also starts at around 0.72 and increases sharply until about epoch 5, after which it levels off and remains relatively flat.
 - Stays around 0.78 for the remaining epochs.
 - The validation accuracy is consistently lower than the training accuracy, suggesting that the model performs better on the training data compared to the validation data.

* **Trend Analysis:**
 - Both training and validation accuracies show an initial sharp increase, indicating that the model is learning effectively in the early epochs.
 - The plateau in validation accuracy after epoch 5 suggests that the model’s ability to generalize to new, unseen data does not improve significantly after this point, which could indicate overfitting.

Overall, the graph shows that while the model is learning well from the training data, its performance on validation data does not improve as much after the initial epochs. This suggests that further tuning might be needed to improve generalization and reduce overfitting.
