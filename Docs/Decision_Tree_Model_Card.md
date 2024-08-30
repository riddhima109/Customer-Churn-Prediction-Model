# Decision Tree Model Card
## Model Details
**Model Name:** Customer Churn Prediction Model

**Developer:** Riddhima Bansal

**Model Date:** August 10, 2024

**Model Version:** 1.0

**Model Type:** Decision Tree - Classification Model

**Model Framework:** scikit-learn / sklearn

## Model Objective
This Decision Tree model is developed to predict customer churn in a telecommunications context. By identifying at-risk customers, the model supports proactive retention efforts, aiming to reduce churn rates and enhance customer loyalty.

**Use Case:**
* **Primary Goal**: Predict customer churn to facilitate targeted interventions.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams within the telecommunications industry.

## Model Input & Output
* **Input:** The Decision Tree model uses customer demographics, account status, service usage, and billing information, which are numerically encoded or categorized.
* **Output:** The output is a binary indicator (0 or 1) where 1 indicates a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn

## Model Architecture: 
#### Algorithm:
The Decision Tree model creates a tree-like structure where internal nodes represent feature tests, branches represent outcomes of these tests, and leaf nodes represent class labels. The model splits the data based on the feature that provides the best split according to criteria like Gini impurity or Information Gain, allowing it to make decisions based on feature values.

**Feature Engineering:**

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were scaled for consistency.
* Missing values were handled through imputation or removal to ensure data quality.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Includes customer demographics, service subscriptions, account status, and churn indicators.
* Split: The data was divided into training (70%) and testing (30%) sets for model evaluation.

#### Evaluation Data:
* Consistency: The same preprocessing pipeline was applied to the test set to ensure a reliable assessment of model performance.

## Performance Metrics:
The Decision Tree model's performance is measured using various metrics calculated on the test dataset after training:

Accuracy: 73%

Precision: 51%

Recall: 50%

F1-Score: 51%

AUC-ROC: 66%

**Evaluation:**
**Confusion Matrix:** Provides insights into the model's classification accuracy by showing counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Illustrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.85 indicating good performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/bd1da21a-e7d1-484f-a180-71c210dda494)


## Limitations
* Decision Trees can be prone to overfitting, especially with complex trees that model noise in the training data.
* The model's interpretability can become challenging with deeper trees or numerous features.

**Alternative Approaches:**
Consider ensemble methods like Random Forests or Gradient Boosting for improved performance and generalization.

## Trade-offs
Decision Trees are easy to interpret and visualize, but they can overfit training data and may not generalize well on unseen data without proper pruning. Ensemble methods can address some of these limitations by combining multiple trees to improve accuracy and robustness.

## Ethical Considerations
* **Bias and fairness:** Ensuring that the Decision Tree model does not exhibit unfair bias towards specific customer groups is crucial. Performance metrics are monitored across different segments to promote fairness.

## Deployment and Maintenance
* **Deployment Strategy:**
  - Initial Deployment: The model is used to support decision-making for customer retention by identifying high-risk customers.
  - Maintenance: Regular updates and retraining with new data are recommended to ensure the model remains accurate and relevant.

* **Model Monitoring:**
  - Performance Tracking: Continuous monitoring of model performance is necessary to detect and address any issues in prediction accuracy.
  - Ethical Monitoring: Regular reviews ensure that the model’s outputs remain fair and unbiased, with updates made as necessary.

## Caveats and Recommendations
* **Model Limitations:** Decision Trees can be sensitive to changes in the training data and may require tuning to avoid overfitting. For improved performance, consider using ensemble methods like Random Forests or Gradient Boosting.
* **Usage Recommendations:** Suitable for scenarios requiring interpretable models and quick insights. For more complex datasets or scenarios, complementary models might provide better performance.
