# Classification Report:

![image](https://github.com/user-attachments/assets/e5ed8c47-d5c6-43f0-94b9-0453216f4ffb)

### **Performance Metrics for DNN Model on Churn Prediction**

**1. Accuracy: 0.80**
- **Definition**: Accuracy is the proportion of correctly predicted instances (both churned and non-churned) out of the total instances.
- **Interpretation**: An accuracy of 80% means the DNN model correctly predicted the churn status for 80% of the customers. This is a solid performance, indicating that the model performs well in general.

**2. Precision: 0.653**
- **Definition**: Precision measures the proportion of true positive predictions among all positive predictions made by the model.
- **Interpretation**: A precision of 65.3% means that when the model predicts a customer will churn (Class 1), it is correct about 65.3% of the time. This reflects a moderate level of confidence in predicting churned customers.

**3. Recall: 0.589**
- **Definition**: Recall measures the proportion of actual positive instances that the model correctly identifies.
- **Interpretation**: A recall of 58.9% indicates that the model correctly identifies approximately 58.9% of the actual churned customers. This lower recall suggests that the model misses some of the churned customers, which could be critical for retention efforts.

**4. F1 Score: 0.619**
- **Definition**: The F1 score is the harmonic mean of precision and recall, providing a balanced measure of the model’s performance, especially when dealing with imbalanced datasets.
- **Interpretation**: An F1 score of 61.9% reflects a moderate balance between precision and recall. It indicates that the model's performance in identifying churned customers is reasonable but can be improved.

# Confusion Matrix:

![image](https://github.com/user-attachments/assets/e559d737-d853-452a-95e3-69079943d496)

   - **True Negatives (TN) = 680**:
     - Customers who did not churn and were correctly predicted as not churned.
   - **False Positives (FP) = 90**:
     - Customers who did not churn but were incorrectly predicted as churned.
   - **False Negatives (FN) = 118**:
     - Customers who did churn but were incorrectly predicted as not churned.
   - **True Positives (TP) = 169**:
     - Customers who did churn and were correctly predicted as churned.

### **Key Insights:**

1. **High True Negatives (680):**
   - The model is effective at identifying non-churned customers, which helps in avoiding unnecessary retention efforts for customers who are not at risk.

2. **Moderate True Positives (169):**
   - The model correctly identifies churned customers, but the recall suggests that there is room for improvement in capturing more churned customers.

3. **Moderate Precision (65.3%):**
   - When the model predicts churn, it is correct around 65.3% of the time, which is decent but could be enhanced with further tuning.

4. **Moderate Recall (58.9%):**
   - The model identifies around 58.9% of actual churned customers. Improving recall would be crucial for better targeting of at-risk customers.

5. **False Positives (90) and False Negatives (118):**
   - The model has a moderate number of false positives and false negatives, which impacts its overall effectiveness in predicting churn.

# Graphs
## Loss Curve
![image](https://github.com/user-attachments/assets/2bf51257-a3d4-4981-8595-d98c9ce2d431)

* Train Loss: This line shows the loss on the training dataset. It starts at approximately 0.575 and decreases steadily to around 0.425 by the 20th epoch. This indicates that the model is learning and improving its predictions on the training data over time.
* Validation Loss: This line represents the loss on the validation dataset. It starts slightly higher than the train loss but decreases sharply, intersecting with the train loss around the 5th epoch and ending slightly above the train loss at the 20th epoch. This suggests that the model is generalizing well to unseen data, as the validation loss is decreasing and closely following the train loss.

## Accuracy Curve
![image](https://github.com/user-attachments/assets/77a2dfb8-603f-4bf0-bee5-2ef3c84be3c8)

* Train Accuracy: This line shows the accuracy on the training dataset. It starts at about 0.74 and increases steadily to just above 0.8 by the 20th epoch. This indicates that the model’s predictions on the training data are becoming more accurate over time.
* Validation Accuracy: This line represents the accuracy on the validation dataset. It starts just below 0.76 and quickly increases to meet the train accuracy around the 5th epoch, continuing closely together until the 20th epoch. This suggests that the model is performing well on unseen data, as the validation accuracy is improving and closely following the train accuracy.

## Summary
Overall, these graphs indicate that the DNN is learning effectively and generalizing well to new data. The close alignment of the training and validation curves suggests that the model is not overfitting and is likely to perform well on real-world data.

# To interpret the results of your churn prediction model, you can consider the following aspects:

![image](https://github.com/user-attachments/assets/91f1362e-df4d-4cf2-99d3-c84081b0ec8b)

### 1. **Binary Predictions**
The model output is a list of binary predictions, where each entry is either `0` or `1`. In this context:
- `0` typically represents a prediction of "no churn" (i.e., the customer will not churn).
- `1` represents a prediction of "churn" (i.e., the customer will churn).

### 2. **Output**
Given the sample output `[0, 1, 0, 0, 0]`, this means:
- For the first sample, the model predicts the customer will **not** churn.
- For the second sample, the model predicts the customer **will** churn.
- For the third to fifth samples, the model predicts the customers will **not** churn.

### 3. **Thresholding**
I used a threshold of 0.5 to convert predicted probabilities into binary predictions. This threshold is commonly used:
- **Probability >= 0.5**: Classified as `1` (churn).
- **Probability < 0.5**: Classified as `0` (no churn).

