# Convolutional Neural Network (CNN) Model Card
## Model Details
**Model Name:** Customer Churn Prediction Model

**Developer:** Riddhima Bansal

**Model Date:** August 10, 2024

**Model Version:** 1.0

**Model Type:** Convolutional Neural Network - Classification Model

**Model Framework:** TensorFlow / Keras

## Model Objective
This Convolutional Neural Network (CNN) model is designed to predict customer churn in a telecommunications setting. By identifying customers likely to churn, the model supports targeted retention strategies, reducing churn rates and enhancing customer loyalty.

**Use Case:**
* **Primary Goal**: Predict customer churn to enable proactive retention strategies.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams within the telecommunications industry.

## Model Input & Output
* **Input:** The CNN model processes structured customer data, including demographics, account status, service usage, and billing information. The data is transformed into a 2D matrix form suitable for convolutional layers.
* **Output:** The model provides a binary classification (0 or 1) where 1 indicates a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn

## Model Architecture: 
#### Algorithm:
The Convolutional Neural Network (CNN) is typically used for image data but can be adapted to structured data by treating it as a 2D matrix. The model consists of convolutional layers that apply filters to extract patterns, followed by pooling layers to reduce dimensionality, and fully connected layers for final classification.

**Feature Engineering:**

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were standardized to ensure uniformity across inputs.
* Data was reshaped into a 2D format to facilitate convolutional processing.

#### Network Architecture:
* **Input Layer:** Handles the reshaped 2D input data, with each cell corresponding to a feature value.
* **Convolutional Layers:** Apply filters to extract local patterns in the data, capturing spatial relationships.
* **Pooling Layers:** Reduce the dimensionality of the data while retaining the most important information.
* **Fully Connected Layers:** Flatten the pooled feature maps and connect to the output layer for final classification.
* **Output Layer:** A single neuron activated by a sigmoid function to produce a probability output for binary classification.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Includes customer demographics, service subscriptions, account status, and churn indicators. The data is reshaped into 2D matrices for CNN processing.
* Split: The data was divided into training (70%) and testing (30%) sets for evaluation.

#### Evaluation Data:
* Consistency: The same preprocessing steps were applied to the test set, ensuring consistency in model evaluation.

## Performance Metrics:
The CNN model's performance is measured using various metrics calculated on the test dataset after training:

Accuracy: 81%

Precision: 70%

Recall: 54%

F1-Score: 61%

**Evaluation:**
**Confusion Matrix:** Provides insights into the model's classification accuracy by showing counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Illustrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.93 indicating strong performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/9ca99b7a-69f3-4483-bc18-af7ecabf37d6)

## Limitations
* CNNs require substantial computational resources, particularly for large datasets or when experimenting with different architectures.
* They are typically used for image data, so their application to structured data requires careful data preprocessing and transformation.

**Alternative Approaches:**
Consider using models like RNNs for handling sequential data or simpler models like Random Forests for interpretability and computational efficiency.

## Trade-offs
CNNs excel at capturing spatial patterns and interactions between features, but they are more complex and resource-intensive compared to simpler models. They also require careful tuning to achieve optimal performance.

## Ethical Considerations
* **Bias and fairness:** Ensuring that the CNN model does not introduce or amplify biases towards any specific customer group is crucial. Performance metrics are monitored across different segments to promote fairness.

## Deployment and Maintenance
* **Deployment Strategy:**
  - Initial Deployment: The model is intended for use as a decision-support tool for prioritizing retention efforts towards high-risk customers.
  - Maintenance: Regular retraining with new data is recommended to maintain model accuracy and relevance.

* **Model Monitoring:**
  - Performance Tracking: Continuous monitoring of the model’s performance is essential to detect and mitigate any drift in prediction accuracy.
  - Ethical Monitoring: Regular reviews ensure that the model’s outputs remain fair and unbiased, with necessary updates made as needed.

## Caveats and Recommendations
* **Model Limitations:** CNNs, while powerful, require significant computational resources and are less interpretable compared to simpler models. They are most effective when applied to data that can be represented in a spatial format.
* **Usage Recommendations:** Ideal for scenarios where capturing complex interactions between features is crucial. For more straightforward use cases, consider simpler models like Decision Trees or Logistic Regression.
