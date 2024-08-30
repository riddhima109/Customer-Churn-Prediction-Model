# Support Vector Machine (SVM) 
## Model Details
**Model Name:** Customer Churn Prediction Model - SVM

**Developer:** Riddhima Bansal

**Model Date:** August 30, 2024

**Model Version:** 1.0

**Model Type:** Support Vector Machine - Classification Model

**Model Framework:** scikit-learn / sklearn

## Model Objective
This Support Vector Machine (SVM) model is designed to predict customer churn in a telecommunications setting. By accurately identifying customers at risk of leaving, the model supports targeted retention strategies, aiming to reduce churn rates and enhance customer loyalty.

**Use Case:**
* **Primary Goal**: Predict customer churn to implement targeted retention measures.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams within the telecommunications industry.

## Model Input & Output
* **Input:** The SVM model takes as input customer demographics, account status, service usage, and billing information, which are numerically encoded or categorized for model processing.
* **Output:** The model outputs a binary indicator (0 or 1), where 1 signifies a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn

## Model Architecture: 
#### Algorithm:
The SVM model utilizes a hyperplane to separate data points into different classes. It aims to find the optimal hyperplane that maximizes the margin between the classes. In cases of non-linear data, the kernel trick can be used to project data into higher-dimensional space for better separation.

**Feature Engineering:**

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were standardized to ensure uniformity across inputs.
* Missing values were addressed through imputation or removal to maintain data quality.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Includes customer demographics, service subscriptions, account status, and churn indicators.
* Split: The data was divided into training (80%) and testing (20%) sets for model evaluation.

#### Evaluation Data:
* Consistency: The same preprocessing pipeline was applied to the test set to ensure a fair assessment of model performance.

## Performance Metrics:
The SVM model's performance is measured using various metrics calculated on a test dataset after training:

Accuracy: 83%

Precision: 72%

Recall: 60%

F1-Score: 66%

AUC-ROC: 89%

**Evaluation:**
**Confusion Matrix:** Provides insights into the model's classification accuracy by displaying counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Demonstrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.89 indicating good performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/d636e67a-b76a-401d-8091-1f483ed39f21)

## Limitations
* SVMs can be computationally intensive, especially with large datasets and high-dimensional feature spaces.
* The choice of kernel function and hyperparameters can significantly affect performance, requiring careful tuning.

**Alternative Approaches:**
Consider models like Logistic Regression, Random Forest, or Neural Networks for different trade-offs in terms of complexity and performance.

## Trade-offs
While SVMs are effective in handling high-dimensional data and providing robust classification, they can be less interpretable and more computationally demanding compared to simpler models like Logistic Regression.

## Ethical Considerations
* **Bias and fairness:** Ensuring the model is free from unfair bias towards any customer group is crucial. Performance metrics are monitored across various segments to promote fair treatment.

## Deployment and Maintenance
* **Deployment Strategy:**
 - Initial Deployment: Intended as a decision-support tool for customer relationship teams to prioritize high-risk customers.
 - Maintenance: Regular retraining with updated customer data is recommended to maintain accuracy and relevance.

* **Model Monitoring:**
 - Performance Tracking: Ongoing monitoring of model performance is necessary to detect and address any prediction accuracy drift.
 - Ethical Monitoring: Continuously review the model’s outputs to ensure they remain fair and unbiased, making updates as needed.

## Caveats and Recommendations
* **Model Limitations:** SVMs may require substantial computational resources and parameter tuning. For complex datasets, exploring alternative models like Random Forests or Neural Networks might be beneficial.
* **Usage Recommendations:** Suitable for scenarios requiring robust classification with high-dimensional data, but might need complementary models for a comprehensive analysis.

---
