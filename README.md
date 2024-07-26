# Credit-card-Fraud-detection


The Credit Card Fraud Detection project aims to identify fraudulent credit card transactions using machine learning techniques. Here's an overview of the entire project:

1. Dataset Overview
The dataset contains transactions made by European cardholders in September 2013.
It includes 284,807 transactions, with 492 identified as fraudulent.
The dataset is highly imbalanced, with fraudulent transactions making up only 0.172% of the total.
Features V1 to V28 are the result of PCA transformations. 'Time' and 'Amount' are the only features not transformed by PCA.
The target variable 'Class' indicates whether a transaction is fraudulent (1) or not (0).
2. Data Preprocessing
Null Value Check: Confirmed no null values in the dataset.
Class Balance Check: Illustrated the imbalance in the dataset, with fraud cases being significantly less than non-fraud cases.
Scaling: Applied RobustScaler to 'Amount' and 'Time' to handle outliers effectively.
3. Data Splitting
Separated the original dataframe to create a training and testing set (80% training, 20% testing).
Implemented random under-sampling to balance the dataset by reducing the majority class.
4. Exploratory Data Analysis (EDA)
Distribution Analysis: Visualized the distributions of 'Amount' and 'Time' features.
Correlation Analysis: Generated correlation matrices to identify features strongly correlated with fraudulent transactions.
Boxplots: Created boxplots to analyze the distribution of features with strong correlations to fraud cases.
5. Outlier Detection and Treatment
Identified and treated outliers in features V10, V12, and V14 using the Interquartile Range (IQR) method to maintain data quality.
Created a copy of the dataset to preserve the original data before removing outliers.
6. Model Training and Evaluation
Implemented several machine learning algorithms:
Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Classifier (SVC)
Decision Tree Classifier
Evaluated the models using cross-validation, calculating training and testing accuracy, ROC AUC scores, precision, recall, and F1 scores.
7. Hyperparameter Tuning
Used GridSearchCV to find the best hyperparameters for the models, particularly for Logistic Regression, KNN, SVC, and Decision Tree.
8. Cross-Validation with Sampling Techniques
Highlighted the issue of data leakage and overfitting when sampling techniques are applied before cross-validation.
Implemented NearMiss for under-sampling and SMOTE (Synthetic Minority Over-sampling Technique) for over-sampling during cross-validation.
9. Neural Network Implementation
Built a simple neural network with two hidden layers using Keras to test the performance on under-sampled and over-sampled data.
10. Performance Metrics
Evaluated models based on accuracy, precision, recall, F1 score, and ROC AUC.
Generated precision-recall curves to visualize the trade-off between precision and recall for different models and sampling techniques.
Key Takeaways:
The project addresses the challenge of class imbalance by employing various sampling techniques and carefully evaluating models to avoid overfitting.
Outlier detection and treatment are crucial for maintaining data quality and ensuring the robustness of the models.
Hyperparameter tuning and cross-validation are essential steps in optimizing model performance.
The final models are evaluated using multiple metrics to ensure a comprehensive assessment of their performance.
The approach combines data preprocessing, exploratory analysis, and advanced machine learning techniques to build effective models for detecting fraudulent transactions.
