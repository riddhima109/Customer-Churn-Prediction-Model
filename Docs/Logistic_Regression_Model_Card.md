# Logistic Regression Model Card
## Model Details
**Model Name:** Customer Churn Prediction Model

**Developer:** Riddhima Bansal

**Model Date:** August 10, 2024

**Model Version:** 1.0

**Model Type:** Logistic Regression - Classification Model

**Model Framework:** scikit-learn / sklearn

## Model Objective
This Logistic Regression model is developed to predict customer churn in a telecommunications setting. By identifying customers at risk of leaving, the model facilitates proactive targeted retention strategies, helping to reduce churn rates and improve customer loyalty.

**Use Case:**
* **Primary Goal**: Predict customer churn to enable targeted interventions.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams within the telecommunications sector.

## Model Input & Output
* **Input:** Inputs to the Logistic Regression model include customer demographics, account status, service usage, and billing information, all of which are numerically encoded or categorized for model ingestion.
* **Output:** The output is a binary indicator (0 or 1) where 1 indicates a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn
  
## Model Architecture: 
#### Algorithm:
The model utilizes a logistic function to estimate the probability of a customer churning. The logistic regression algorithm is well-suited for binary classification, particularly where the relationship between the input features and the target variable is approximately linear, estimating probabilities that can be thresholded at 0.5 for classification.
Feature Engineering:

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were standardized to ensure uniformity across inputs.
* Missing values were handled through imputation or removal to maintain data integrity.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Includes data on customer demographics, service subscriptions, account status, and churn indicators.
* Split: The data was split into training (80%) and testing (20%) sets to evaluate model performance.

#### Evaluation Data:
* Consistency: The same preprocessing pipeline was applied to the test set to ensure consistency in model evaluation.

## Performance Metrics:
The Logistic Regression model's performance is quantified through various metrics calculated on a test dataset after training:

Accuracy: 81%

Precision: 69%

Recall: 55%

F1-Score: 61%

AUC-ROC: 86%

**Evaluation:**
**Confusion Matrix:** Provides insight into the model's classification accuracy by showing the counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Illustrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.74 indicating moderate performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/d636e67a-b76a-401d-8091-1f483ed39f21)

## Limitations
* Logistic Regression assumes a linear relationship between the independent variables and the log-odds of the dependent variable, which might not hold in complex scenarios like customer behavior patterns.
* The model's performance can degrade if confronted with highly non-linear data without adequate feature engineering.

**Alternative Approaches:**
Consider more complex models like Random Forest, Gradient Boosting, or Neural Networks for scenarios requiring the capture of intricate patterns in data.

## Trade-offs
While Logistic Regression is computationally efficient and interpretable, it might not capture complex patterns as effectively as more sophisticated models like Random Forests or Neural Networks.
The simplicity of the model allows for quick iterations and is useful for baseline modeling, but it may require more feature engineering to match the performance of other algorithms in non-linear contexts.

## Ethical Considerations
* **Bias and fairness:** Care has been taken to ensure that the model does not exhibit unfair bias towards any particular group of customers. Performance metrics are monitored across different segments to ensure equitable treatment.

## Deployment and Maintenance
* **Deployment Strategy:**
 - Initial Deployment: The model is intended for use as a decision-support tool, helping customer relationship teams prioritize interventions.
 - Maintenance: Regular model retraining is advised as new customer data becomes available to ensure continued accuracy and relevance.

* **Model Monitoring:**
 - Performance Tracking: Continuous monitoring of model performance is essential to detect and mitigate any drift in prediction accuracy.
 - Ethical Monitoring: Ensure that the model’s outputs remain fair and unbiased over time, with updates made to address any issues.
## Caveats and Recommendations
* **Model Limitations:** Given the logistic regression’s limitations in handling non-linear relationships, it's advisable to explore more complex models if improvements in predictions are required.
* **Usage Recommendations:** Ideal for use as a preliminary model to identify at-risk customers before applying more complex algorithms for deeper insights.
