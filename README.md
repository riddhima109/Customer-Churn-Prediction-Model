# Customer-Churn-Prediction-Model
This repository contains machine learning models developed to predict customer churn in a telecommunications company—the phenomenon where customers stop using a company's products or services over a given period.The goal of these models is to identify customers likely to churn so that proactive strategies can be employed to retain them. The project employs various algorithms on the Telco Customer Churn dataset to analyze customer behavior and transaction data, identifying key indicators of churn. Algorithms implemented include Random Forest Classifier, Logistic Regression, Decision Tree, SVM, and KNN. This project includes detailed Google Colab Notebooks focusing on each step of the process—from data preprocessing and exploratory data analysis to model training and evaluation.The goal is to develop a predictive model that can help businesses understand and mitigate customer churn, ultimately enhancing customer retention strategies.

# Components of the Repository
-Data: Original dataset and preprocessed data files.

Notebooks: Step-by-step Jupyter notebooks covering data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning using Bayesian optimization, and model evaluation.

Model Card and Datasheet: Documentation providing details on model performance, usage, and dataset characteristics.

Results: Visualizations and output files showcasing the analysis and outcomes of the models.
Data
The dataset used in this project is the Telco Customer Churn dataset. It can be found in the data directory. This dataset includes customer data from a telecom company, where the main goal is to predict customer churn based on various features like monthly charges, tenure, and service type.

Datasheet for Telco Customer Churn Dataset: This datasheet provides detailed information about the motivations, composition, collection process, and pre-processing steps involved with the Telco Customer Churn dataset. It is essential for understanding the scope, limitations, and appropriate uses of the data.

Models
The models used include Random Forest, Logistic Regression, and Neural Networks. Random Forest was chosen for its robustness against overfitting, Logistic Regression for its efficacy in binary outcomes, and Neural Networks for their ability to model complex relationships in high-dimensional data.

Random Forest
Description: Utilizes ensemble learning technique for classification. Random Forest is robust against overfitting as it uses multiple decision trees to make predictions.
Performance: Details about the accuracy, precision, recall, and F1-score are documented in the Random Forest model card.
Logistic Regression
Description: A statistical model that estimates the probability of a binary outcome based on input features. It is useful for understanding the influence of several independent variables on a binary outcome.
Performance: Metrics and evaluation are available in the Logistic Regression model card.
Neural Network
Description: Employs a deep learning architecture to model complex relationships in data. The model used here is a fully connected deep neural network, structured to capture intricate patterns in customer behavior.
Performance: Evaluation results can be found in the Neural Network model card.
Hyperparameter Optimization
Hyperparameters were optimized using Bayesian Optimization. This method was selected for its efficiency in finding the best hyperparameters by building a probability model of the objective function and using it to select the most promising hyperparameters to evaluate in the true objective function.

Results
The models achieved varying levels of accuracy, with Logistic Regression performing the best. The results help in understanding which features most significantly predict churn, such as tenure and monthly charges. These insights assist in developing targeted interventions to reduce customer churn.

Model Accuracy Plot

Model Cards
Model cards for each algorithm are included in this repository to provide insights into model performance, usage, and limitations.

Random Forest Model Card
Logistic Regression Model Card
Neural Network Model Card
