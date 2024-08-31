# Classification Report:

![image](https://github.com/user-attachments/assets/958ebf3c-64d1-4ce2-93c9-48ae50345ce3)

#### **Classification Metrics**

- **Precision:**
  - **Class 0 (No Churn)**: 0.84
    - Out of all instances predicted as no churn, 84% were actually no churn.
  - **Class 1 (Churn)**: 0.66
    - Out of all instances predicted as churn, 66% were actually churn.

- **Recall:**
  - **Class 0 (No Churn)**: 0.89
    - Out of all actual no churn instances, 89% were correctly identified.
  - **Class 1 (Churn)**: 0.58
    - Out of all actual churn instances, 58% were correctly identified.

- **F1-Score:**
  - **Class 0 (No Churn)**: 0.86
    - A balanced measure of precision and recall for non-churn cases.
  - **Class 1 (Churn)**: 0.62
    - A balanced measure of precision and recall for churn cases.

- **Accuracy:**
  - Overall: 0.80
    - The proportion of total correct predictions (both churn and no churn) out of all predictions.

- **Macro Average:**
  - **Precision**: 0.75
  - **Recall**: 0.73
  - **F1-Score**: 0.74
    - Averages across classes, treating all classes equally, regardless of their frequency.

- **Weighted Average:**
  - **Precision**: 0.79
  - **Recall**: 0.80
  - **F1-Score**: 0.80
    - Averages across classes, weighted by the number of true instances of each class.

#### **Detailed Analysis**

- **Model Performance on Class 0 (No Churn):**
  - **High Recall (0.89)**: The model is good at identifying non-churn cases, minimizing false negatives for this class.
  - **Good Precision (0.84)**: When the model predicts no churn, it's accurate 84% of the time.
  - **High F1-Score (0.86)**: This suggests a good balance between precision and recall for class 0.

- **Model Performance on Class 1 (Churn):**
  - **Moderate Recall (0.58)**: The model misses a significant portion of actual churn cases (false negatives).
  - **Moderate Precision (0.66)**: When the model predicts churn, it is accurate 66% of the time.
  - **Moderate F1-Score (0.62)**: The balance between precision and recall is less favorable for churn cases, indicating room for improvement.

- **Overall Accuracy (0.80):**
  - The model's overall performance is solid, but the disparity between precision and recall for churn cases suggests that the model is more conservative in predicting churn to avoid false positives.

- **Macro vs. Weighted Averages:**
  - **Macro Average**: Shows average performance treating all classes equally. This metric indicates that the model is slightly better at predicting no churn compared to churn.
  - **Weighted Average**: Adjusts the averages based on the frequency of each class in the dataset, which indicates that the model performs better when accounting for the class distribution.


 # Confusion Matrix:

 ![image](https://github.com/user-attachments/assets/ee6996e8-a5e3-48f5-84f8-4e6bbcf1cc55)

- **True Negatives (TN)**: 674
  - These are correctly predicted non-churn instances.
- **False Positives (FP)**: 87
  - These are incorrectly predicted churn instances (the model predicted churn, but the actual class was no churn).
- **False Negatives (FN)**: 124
  - These are incorrectly predicted non-churn instances (the model predicted no churn, but the actual class was churn).
- **True Positives (TP)**: 172
  - These are correctly predicted churn instances.

# Graphs

## Loss Graph:

![image](https://github.com/user-attachments/assets/fea613bb-69b3-47dc-8349-febd47c785a2)

**Graph Overview**
* **X-axis (Epochs):** Represents the number of training iterations.
* **Y-axis (Loss):** Indicates the loss value, which measures how well the model’s predictions match the actual outcomes. Lower loss values are better.

**Lines**
* **Blue Line (Train):** Represents the loss on the training dataset.
* **Orange Line (Validation):** Represents the loss on the validation dataset.

**Key Observations**
* **Decreasing Loss:** Both the training and validation loss decrease as the number of epochs increases. This indicates that the model is learning and improving its predictions over time.
* **Convergence:** The training and validation loss values converge towards a similar value (around 0.400) after approximately 80 epochs. This suggests that the model is not overfitting, as the validation loss does not increase or diverge from the training loss.
* **Initial Loss Values:** At epoch 0, the training loss starts around 0.575, and the validation loss is slightly higher. This is typical as the model begins with random weights and gradually improves.

**Conclusion**
The graph indicates that the RNN model is effectively learning from the churn dataset, with both training and validation losses decreasing and converging over time. This suggests good generalization to unseen data, which is crucial for making accurate predictions on new customer data.

## Accuracy Graph:

![image](https://github.com/user-attachments/assets/a5a936c9-0ca8-460e-927e-177b91f46bd2)

**Graph Overview**
* **X-axis (Epochs):** Represents the number of training iterations.
* **Y-axis (Accuracy):** Indicates the accuracy of the model’s predictions. Higher accuracy values are better.

**Lines**
* **Blue Line (Train):** Represents the accuracy on the training dataset.
* **Orange Line (Validation):** Represents the accuracy on the validation dataset.

**Key Observations**
* **Increasing Accuracy:** Both the training and validation accuracy increase as the number of epochs increases. This indicates that the model is learning and improving its predictions over time.
* **Initial Accuracy Values:** At epoch 0, the training accuracy starts below 0.78, and the validation accuracy starts around 0.76. Both accuracies rise sharply in the initial epochs.
* **Plateauing:** The training accuracy plateaus slightly above 0.8, while the validation accuracy plateaus just above the training accuracy after around 50 epochs. This suggests that the model has reached a stable performance level.

**Conclusion**
The graph indicates that the RNN model is effectively learning from the churn dataset, with both training and validation accuracies increasing and stabilizing over time. The validation accuracy being slightly higher than the training accuracy suggests good generalization to unseen data, which is crucial for making accurate predictions on new customer data.

# Class Probabilities for Test Instances:

![image](https://github.com/user-attachments/assets/ba776bfc-de14-4fc4-af5d-8b600d13acaf)

These probabilities reflect the model's confidence in predicting the positive class (churn) for each instance:
- **Instance 1**: Probability of churn = 0.0397 (low confidence)
- **Instance 2**: Probability of churn = 0.3777 (moderate confidence)
- **Instance 3**: Probability of churn = 0.0414 (low confidence)
- **Instance 4**: Probability of churn = 0.0601 (low confidence)
- **Instance 5**: Probability of churn = 0.5783 (high confidence)

# Binary Predictions After Applying Threshold of 0.5:

![image](https://github.com/user-attachments/assets/5a50a5da-f564-44c7-bb67-6c0ae9147127)

- **Instance 1**: Predicted as no churn (0), as probability < 0.5
- **Instance 2**: Predicted as no churn (0), as probability < 0.5
- **Instance 3**: Predicted as no churn (0), as probability < 0.5
- **Instance 4**: Predicted as no churn (0), as probability < 0.5
- **Instance 5**: Predicted as churn (1), as probability ≥ 0.5
