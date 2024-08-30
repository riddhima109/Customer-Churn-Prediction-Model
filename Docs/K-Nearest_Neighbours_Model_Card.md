Here's a model card for a K-Nearest Neighbors (KNN) model for customer churn prediction:

---

# K-Nearest Neighbors (KNN) Model Card
## Model Details
**Model Name:** Customer Churn Prediction Model - KNN

**Developer:** Riddhima Bansal

**Model Date:** August 30, 2024

**Model Version:** 1.0

**Model Type:** K-Nearest Neighbors - Classification Model

**Model Framework:** scikit-learn / sklearn

## Model Objective
This K-Nearest Neighbors (KNN) model is designed to predict customer churn in a telecommunications context. By identifying customers likely to leave, the model supports targeted retention efforts, aiming to lower churn rates and enhance customer retention strategies.

**Use Case:**
* **Primary Goal**: Predict customer churn to enable effective intervention strategies.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams in the telecommunications industry.

## Model Input & Output
* **Input:** Inputs to the KNN model include customer demographics, account status, service usage, and billing information, all of which are numerically encoded or categorized.
* **Output:** The output is a binary indicator (0 or 1) where 1 signifies a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn

## Model Architecture: 
#### Algorithm:
The KNN model classifies data points based on the majority class among the 'k' nearest neighbors in the feature space. The distance metric (e.g., Euclidean) is used to determine the proximity of neighbors. KNN is a non-parametric method that does not assume a specific form for the decision boundary.

**Feature Engineering:**

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were scaled to ensure uniformity across inputs.
* Missing values were handled through imputation or removal to ensure data quality.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Contains data on customer demographics, service subscriptions, account status, and churn indicators.
* Split: The data was partitioned into training (80%) and testing (20%) sets for performance evaluation.

#### Evaluation Data:
* Consistency: The same preprocessing procedures were applied to the test set to ensure reliable model evaluation.

## Performance Metrics:
The KNN model's performance is measured using various metrics calculated on the test dataset after training:

Accuracy: 77%

Precision: 58%

Recall: 54%

F1-Score: 56%

AUC-ROC: 80%

**Evaluation:**
**Confusion Matrix:** Offers insights into the model's classification performance by showing counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Demonstrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.82 indicating good performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/10eb5d1a-e425-4b89-b5be-8721c4fbc6fb)


## Limitations
* KNN can be computationally intensive during prediction, especially with large datasets, as it requires distance calculations for all data points.
* The performance of KNN can be significantly affected by the choice of 'k' and the distance metric.

**Alternative Approaches:**
Consider models like Logistic Regression, Random Forest, or SVM for different trade-offs in terms of complexity and performance.

## Trade-offs
KNN is easy to understand and implement, and it performs well with small datasets. However, it may struggle with larger datasets and high-dimensional data due to increased computational costs and sensitivity to irrelevant features.

## Ethical Considerations
* **Bias and fairness:** Ensuring that the KNN model does not exhibit bias towards any specific customer group is important. Performance metrics are reviewed across various segments to maintain fairness.

## Deployment and Maintenance
* **Deployment Strategy:**
  - Initial Deployment: The model is used as a decision-support tool to identify high-risk customers for targeted retention efforts.
  - Maintenance: Regular updates and retraining with new customer data are recommended to maintain accuracy and effectiveness.

* **Model Monitoring:**
  - Performance Tracking: Continuous monitoring of model performance is crucial to detect any changes in prediction accuracy.
  - Ethical Monitoring: Regular reviews ensure that the model’s outputs are fair and unbiased, with necessary adjustments made to address any issues.

## Caveats and Recommendations
* **Model Limitations:** KNN's performance can be impacted by the size of the dataset and the choice of hyperparameters. For larger and more complex datasets, exploring other models like Random Forests or Neural Networks might be beneficial.
* **Usage Recommendations:** Ideal for small to medium-sized datasets where the simplicity and interpretability of KNN are advantageous. For larger datasets, additional models may provide better performance.
