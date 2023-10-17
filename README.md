# Data-Science---Naive-Bayes
Data Import and Exploratory Data Analysis (EDA):
The code starts by importing necessary libraries, including Pandas, NumPy, Matplotlib, Seaborn, and scikit-learn modules.
Two datasets, sal_train (training data) and sal_test (testing data), are read from CSV files.
EDA is performed on both datasets to explore their structure, check for missing values, and duplicate rows.

Feature Engineering:
Duplicate rows are removed from both the training and testing datasets.
The 'native' column is dropped from both datasets.

Label Encoding:
Categorical columns in both datasets are label-encoded using scikit-learn's LabelEncoder. This step converts categorical variables into numerical format for model training.
The 'Salary' column is label-encoded, where '0' represents 'Less than 50K' and '1' represents 'Above 50K'.

Feature Importance Analysis:
An ExtraTreesClassifier model is trained on the training data to analyze feature importances. The code identifies which features have the most influence on predicting the target variable ('Salary').

Visualization:
A bar plot is created to visualize feature importances, showing the relevance of each feature in predicting the target variable.

Data Preprocessing:
A subset of columns with the lowest feature importance is dropped from both the training and testing datasets.
The remaining columns ('age', 'capitalgain', 'hoursperweek') are standardized using scikit-learn's StandardScaler.

Model Building:
The Naive Bayes algorithm is employed for classification. A Gaussian Naive Bayes model is trained on the preprocessed training data.

Model Evaluation:
The model's performance is evaluated using a confusion matrix, visualized with a heatmap, and a classification report. The classification report provides metrics such as precision, recall, and F1-score for each class.

Histogram Visualization:
A histogram is plotted to display the predicted probabilities of salaries greater than 50K. This can help assess the spread or concentration of predicted probabilities.

The code provides a comprehensive pipeline for building and evaluating a classification model using Naive Bayes for salary prediction. It also includes comments and explanations for each step to make it more understandable for users.
