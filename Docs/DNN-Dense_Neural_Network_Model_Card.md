# Deep Neural Network (DNN) 
## Model Details
**Model Name:** Customer Churn Prediction Model

**Developer:** Riddhima Bansal

**Model Date:** August 10, 2024

**Model Version:** 1.0

**Model Type:** Deep Neural Network - Classification Model

**Model Framework:** TensorFlow / Keras

## Model Objective
This Deep Neural Network (DNN) model is designed to predict customer churn in a telecommunications context. By identifying customers likely to leave, the model helps in implementing targeted retention strategies, thereby reducing churn rates and improving customer loyalty.

**Use Case:**
* **Primary Goal**: Predict customer churn to enable proactive interventions.
* **Target Users:** Customer Relationship Managers, Data Analysts, Data Science Teams within the telecommunications industry.

## Model Input & Output
* **Input:** The DNN model takes customer demographics, account status, service usage, and billing information as input features, all of which are numerically encoded or categorized.
* **Output:** The model provides a binary classification (0 or 1) where 1 indicates a prediction that the customer will churn and 0 indicates the customer will remain.

Prediction: A binary classification where:

1 = High risk of churn

0 = Low or no risk of churn

## Model Architecture: 
#### Algorithm:
The Deep Neural Network (DNN) is a multi-layered artificial neural network that consists of an input layer, multiple hidden layers, and an output layer. Each layer is composed of neurons that apply weighted sums and activation functions (e.g., ReLU) to model complex relationships between features and the target variable. The model is trained using backpropagation and optimization techniques like stochastic gradient descent.

**Feature Engineering:**

#### Preprocessing Steps:
* Categorical features were encoded using techniques such as One-Hot Encoding.
* Numerical features were standardized for uniformity across inputs.
* Missing values were handled through imputation or removal to maintain data quality.

#### Network Architecture:
* **Input Layer:** Consists of nodes corresponding to each feature in the dataset.
* **Hidden Layers:** Multiple hidden layers with neurons activated by ReLU functions to capture non-linear relationships.
* **Output Layer:** A single neuron activated by a sigmoid function to produce a probability output for binary classification.

## Training and Evaluation Data

#### Training Data:
* Source: Kaggle's Telco Customer Churn dataset.
* Composition: Includes customer demographics, service subscriptions, account status, and churn indicators.
* Split: The data was divided into training (70%) and testing (30%) sets for evaluation.

#### Evaluation Data:
* Consistency: The same preprocessing steps were applied to the test set to ensure consistency in model evaluation.

## Performance Metrics:
The DNN model's performance is measured using various metrics calculated on the test dataset after training:

Accuracy: 80%

Precision: 65%

Recall: 59%

F1-Score: 62%


**Evaluation:**
**Confusion Matrix:** Provides insights into the model's classification accuracy by showing counts of true positives, true negatives, false positives, and false negatives.

**ROC Curve:** Illustrates the trade-off between the true positive rate and the false positive rate, with an AUC of 0.92 indicating strong performance.

## Performance Graph
![image](https://github.com/user-attachments/assets/33256492-131e-44bf-ac1f-d596a79a3647)


## Limitations
* DNNs can be prone to overfitting, particularly with small datasets or insufficient regularization.
* They require substantial computational resources for training and tuning hyperparameters.

**Alternative Approaches:**
Consider simpler models like Logistic Regression or Random Forest if interpretability and computational efficiency are priorities. For more complex scenarios, other deep learning architectures like Convolutional Neural Networks (CNNs) or Recurrent Neural Networks (RNNs) might be explored.

## Trade-offs
Deep Neural Networks offer powerful modeling capabilities for capturing complex patterns and non-linear relationships. However, they can be less interpretable and more resource-intensive compared to simpler models. Proper tuning and regularization are critical to avoid overfitting.

## Ethical Considerations
* **Bias and fairness:** Ensuring that the DNN model does not introduce or amplify bias towards any particular customer group is essential. Performance metrics are monitored across different segments to promote fairness.

## Deployment and Maintenance
* **Deployment Strategy:**
  - Initial Deployment: The model is intended for use as a decision-support tool to prioritize interventions for high-risk customers.
  - Maintenance: Regular retraining with new data is advised to maintain model accuracy and relevance.

* **Model Monitoring:**
  - Performance Tracking: Continuous monitoring of the model's performance is crucial to detect any drift in prediction accuracy.
  - Ethical Monitoring: Regular reviews ensure that the model’s outputs remain fair and unbiased, with updates made as needed.

## Caveats and Recommendations
* **Model Limitations:** Deep Neural Networks require careful tuning and can be resource-intensive to train. They also require larger datasets to perform effectively. For smaller datasets, simpler models may be more appropriate.
* **Usage Recommendations:** Best suited for complex datasets where capturing non-linear relationships is crucial. For scenarios requiring high interpretability, simpler models like Decision Trees or Random Forests may be preferred.
