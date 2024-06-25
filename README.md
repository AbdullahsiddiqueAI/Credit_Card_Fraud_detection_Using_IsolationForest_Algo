# Anomaly Detection in Credit Card Transactions
This project focuses on detecting anomalies, specifically fraudulent transactions, in credit card data using machine learning algorithms. The dataset used is from Kaggle and contains anonymized credit card transactions labeled as fraud or normal.

# Dataset
The dataset can be found on Kaggle at the following link:
[Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

# Introduction
The objective is to develop models that can accurately identify fraudulent transactions, which are typically rare compared to normal transactions. Anomalies or outliers in this context are transactions that deviate significantly from the normal behavior.

# Environment Setup
Ensure you have the following libraries installed in your Python environment:

numpy
pandas
scikit-learn
matplotlib
seaborn


# Exploratory Data Analysis (EDA)


# Loading and Understanding the Data
The dataset is loaded from a CSV file using pandas.
Initial exploration includes checking for missing values and understanding the structure of the data.


# Data Visualization
Visualizations such as bar plots and histograms are used to understand the distribution of transaction classes (normal vs. fraud) and transaction amounts.

# Data Preprocessing
Sampling and Splitting
A 10% sample of the data is used to balance computational cost with representative data.
The dataset is split into features (independent variables) and the target variable ('Class').


# Model Building and Evaluation


# Isolation Forest Algorithm
Objective: Identify anomalies (fraudulent transactions) based on their deviation from the majority of normal transactions.
Working Principle: Isolation Forests build isolation trees that isolate anomalies more quickly due to their lower path lengths in the tree structure.
Local Outlier Factor (LOF) Algorithm
Objective: Detect outliers based on their local density deviation compared to neighbors.
Working Principle: LOF calculates a score indicating how different a data point is from its local neighborhood.
Support Vector Machine (SVM) Algorithm
Objective: Also used for outlier detection, particularly in cases where data is not linearly separable.
Parameters: Kernel, gamma, and nu parameters are adjusted to improve detection performance.
Model Comparison
Each algorithm is evaluated based on its accuracy score and classification report metrics.
Isolation Forest outperforms LOF and SVM in terms of accuracy and precision in detecting fraudulent transactions.


# Conclusion
Isolation Forest proves to be an effective method for detecting anomalies, especially in highly imbalanced datasets like credit card transactions. Further improvements could involve using more complex models or increasing sample sizes for better accuracy.

By leveraging anomaly detection techniques, financial institutions can enhance their ability to identify and prevent fraudulent activities, thereby safeguarding transactions and customer accounts.