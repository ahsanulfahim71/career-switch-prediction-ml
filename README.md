# career-switch-prediction-ml
Machine learning model comparison for predicting career switching behavior
This project applies machine learning techniques to predict whether a professional is likely to switch careers based on demographic, educational, and work-related attributes. The goal is to compare multiple models and evaluate their performance on an imbalanced, real-world dataset.

Problem Statement
Career switching has become increasingly common due to rapid changes in technology and job requirements. Using structured data, this project frames career switching as a binary classification problem and evaluates how different models handle non-linear relationships and class imbalance.

📊 Dataset
Samples: 5,000
Features:
14 raw features
168 features after one-hot encoding
Target: will_change_career (0 = No, 1 = Yes)
Class imbalance:
No switch: 3,738
Switch: 1,262
The dataset includes demographic information, education level, company attributes, training hours, and experience-related variables.

🔍 Exploratory Data Analysis
Key insights from EDA:
No single feature strongly predicts career switching, suggesting a non-linear problem
Higher training hours are associated with a greater likelihood of switching careers
City development index and company-related attributes influence switching behavior
Class imbalance makes accuracy alone an insufficient evaluation metric

🛠️ Data Preprocessing
Missing values handled using:
Mean imputation for numerical features
Mode imputation for categorical features
One-hot encoding applied to categorical variables
Feature scaling using StandardScaler (after train-test split to prevent data leakage)
Identifier column removed
Stratified train-test split (80/20) to preserve class distribution

🤖 Models Trained
Supervised Learning

K-Nearest Neighbors (baseline)
Decision Tree
Multi-Layer Perceptron (Neural Network)

Unsupervised Learning
K-Means clustering (used to explore hidden patterns and structure)

📈 Evaluation Metrics

Due to class imbalance, models were evaluated using:
Accuracy
Precision
Recall
F1-Score
ROC-AUC
