# Customer Churn Prediction Model
This repository contains machine learning and deep learning models developed to predict customer churn in a telecommunications company—the phenomenon where customers stop using a company's products or services over a given period.The goal of these models is to identify customers likely to churn so that proactive strategies can be employed to retain them. The project employs various algorithms on the Telco Customer Churn dataset to analyze customer behavior and transaction data, identifying key indicators of churn. Machine Learning Algorithms implemented include Random Forest Classifier, Logistic Regression, Decision Tree, SVM, and KNN.Deep Learning Algorithms implemented include Deep Neural Network, Recurrent Neural Netowrk-RNN, Convolutional Neural Network, Transformer Model. This project includes detailed Jupyter Notebooks focusing on each step of the process—from data preprocessing and exploratory data analysis to model training and evaluation.The goal is to develop a predictive model that can help businesses understand and mitigate customer churn, ultimately enhancing customer retention strategies.

## Components of the Repository
->[Data](Datasets): Original dataset and preprocessed dataset files.

->[Code-Models-Notebooks](Code-Models-Notebooks): Step-by-step Jupyter notebooks covering data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning, and model evaluation.

->[Model Card and Datasheet(Docs)](Docs): Documentation providing details on model performance, usage, and dataset characteristics.

->[Graphs](Graphs): Visualizations and output files showcasing the analysis and outcomes of the models.

->[Results](Results): The results help in understanding which features most significantly predict churn, such as tenure and monthly charges.

### Data
The dataset used in this project is the Telco Customer Churn dataset. It can be found in the datasets directory. This dataset includes customer data from a telecom company, where the main goal is to predict customer churn based on various features like monthly charges, tenure, and service type.

[Datasheet for Telco-Customer-Churn](https://github.com/riddhima109/Customer-Churn-Prediction-Model/blob/4e2ab028f38c6cf3bbb4fa1220dd482bf3f08f5e/Docs/Datasheet%20for%20Telco-Customer-Churn): This datasheet provides detailed information about the motivations, composition, collection process, and pre-processing steps involved with the Telco Customer Churn dataset. It is essential for understanding the scope, limitations, and appropriate uses of the data.

### Models
The models used in this project include:

#### Machine Learning Algorithms:

**Random Forest Classifier:** Chosen for its robustness against overfitting and its ability to handle large datasets with high dimensionality.
**Logistic Regression:** Selected for its effectiveness in binary classification tasks, providing clear and interpretable results.
**Decision Tree:** Used for its simplicity and transparency, making it easy to understand decision-making processes.
**Support Vector Machine (SVM):** Implemented for its strength in handling classification problems with a clear margin of separation.
**K-Nearest Neighbors (KNN):** Applied for its simplicity and effectiveness in classification tasks based on feature similarity.

#### Deep Learning Algorithms:

**Deep Neural Network (DNN):** Utilized for its ability to model complex relationships in high-dimensional data through multiple hidden layers.
**Recurrent Neural Network (RNN):** Chosen for its capability to handle sequential data and capture temporal dependencies.
**Convolutional Neural Network (CNN):** Implemented for its effectiveness in extracting features from structured grid-like data, such as images.
**Transformer Model:** Used for its powerful performance in capturing long-range dependencies and handling large-scale data.

Each algorithm was selected based on its strengths in addressing different aspects of the customer churn prediction problem, from managing complex data relationships to providing robust and interpretable predictions.

##### Random Forest Classifier
**Description:** Utilizes an ensemble learning technique for classification by combining multiple decision trees. Random Forest is robust against overfitting and performs well with large, high-dimensional datasets by averaging the predictions of individual trees to improve accuracy and stability.
**Performance:** Detailed metrics, including accuracy, precision, recall, and F1-score, are documented in the Random Forest model card.

##### Logistic Regression
**Description:** A statistical model that estimates the probability of a binary outcome based on input features. It is effective for understanding how independent variables impact the probability of a binary result and provides clear, interpretable results.
**Performance:** Metrics and evaluation results are available in the Logistic Regression model card.

##### Decision Tree
**Description:** Implements a simple, tree-like model for classification or regression tasks. It splits the data into branches based on feature values, making it easy to understand and visualize the decision-making process.
**Performance:** Evaluation details, including accuracy and interpretability, are available in the Decision Tree model card.

##### Support Vector Machine (SVM)
**Description:** A classification technique that finds the optimal hyperplane to separate different classes in a high-dimensional space. It is effective for problems with clear margins of separation and works well with both linear and non-linear data.
**Performance:** Performance metrics, including accuracy and margin of separation, are documented in the SVM model card.

##### K-Nearest Neighbors (KNN)
**Description:** A non-parametric classification algorithm that assigns a class to a sample based on the majority class among its nearest neighbors. It is simple to implement and effective for tasks where similarity between samples is key.
**Performance:** Evaluation results, including accuracy and class prediction details, are available in the KNN model card.

##### Deep Neural Network (DNN)
**Description:** Utilizes a deep learning architecture with multiple hidden layers to model complex relationships in high-dimensional data. The fully connected layers capture intricate patterns in customer behavior.
**Performance:** Evaluation results can be found in the Deep Neural Network model card.

##### Recurrent Neural Network (RNN)
**Description:** Designed to handle sequential data and capture temporal dependencies through its recurrent connections. It is suitable for tasks involving sequences, such as time series data.
**Performance:** Metrics and evaluation details are documented in the RNN model card.

##### Convolutional Neural Network (CNN)
**Description:** Effective in extracting features from structured grid-like data, such as images, using convolutional layers to detect spatial hierarchies and patterns.
**Performance:** Detailed performance metrics and results are available in the CNN model card.

##### Transformer Model
**Description:** Leverages self-attention mechanisms to capture long-range dependencies and process sequences in parallel. It is particularly powerful for handling large-scale data and complex relationships.
**Performance:** Evaluation results, including accuracy and ability to handle long-range dependencies, are documented in the Transformer model card.

#### Hyperparameter Optimization
Hyperparameters were optimized using standard grid search or random search methods, focusing on selecting the best configuration through systematic evaluation of various parameter combinations.


Results
The models achieved varying levels of accuracy, with Logistic Regression and CNN performing the best. The results help in understanding which features most significantly predict churn, such as tenure and monthly charges. These insights assist in developing targeted interventions to reduce customer churn.

Model Accuracy Plot

![image](https://github.com/user-attachments/assets/28a43660-8a74-46dc-a7e9-b73c465d1556)

