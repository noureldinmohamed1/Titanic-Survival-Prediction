# Titanic - Survival Prediction Project 🚢

This repository contains a comprehensive End-to-End Machine Learning project for predicting passenger survival on the Titanic. The project implements rigorous data preprocessing, feature engineering, missing value imputation based on statistical grouping, and a comparative evaluation of multiple classification models.

## 🔗 Project Links
*   **Kaggle Notebook:** [Logistic Regression vs Random Forest vs XGBoost](https://www.kaggle.com/code/noureldin23/logistic-regression-vs-random-forest-vs-xgboost)
*   **Dataset Source:** [Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)

---

## 📌 Project Overview
The objective of this project is to build a binary classification model that predicts whether a passenger survived (`1`) or perished (`0`) during the Titanic disaster. 

The workflow involves:
1. **Exploratory Data Analysis (EDA):** Understanding data structures, shapes, distributions, and missing values.
2. **Advanced Feature Engineering:** Extracting titles from names and constructing family-based features (`Family_size`, `Is_alone`).
3. **Smart Data Imputation:** Handling missing values logically (e.g., filling missing ages using the median age of passengers with the same `Title`) to prevent data leakage.
4. **Model Training & Comparison:** Training and tuning Logistic Regression, Random Forest, and XGBoost classifiers.
5. **Evaluation:** Assessing performance using Accuracy, Classification Reports, Confusion Matrices, and ROC-AUC curves.

---

## 🛠️ Tech Stack & Libraries Used
*   **Data Manipulation:** `numpy`, `pandas`
*   **Data Visualization:** `matplotlib`, `seaborn`
*   **Machine Learning (Scikit-Learn):** `GridSearchCV`, `Pipeline`, `ColumnTransformer`, `StandardScaler`, `OneHotEncoder`
*   **Classifiers:** `LogisticRegression`, `RandomForestClassifier`, `XGBClassifier`
*   **Metrics:** `accuracy_score`, `classification_report`, `confusion_matrix`, `roc_auc_score`, `roc_curve`

---

## 📊 Models Comparison & Results

The models were evaluated using standard classification metrics on the test split. Below is the summary of the performance across the different architectures:

| Model | Accuracy | ROC-AUC Score | Comments |
| :--- | :---: | :---: | :--- |
| **Logistic Regression** | **82.68** | **87.22** | **Best Performing Model.** Demonstrates excellent generalization and robustness on the engineered feature set. |
| **XGBoost Classifier** | *79.88* | *86.37* | Strong performance with gradient boosting, slightly following the baseline. |
| **Random Forest** | *79.32* | *85.55* | Robust ensemble tree-based approach, providing stable baseline metrics. |

---

## 🚀 Model Architecture & Training Pipeline
The codebase leverages modern `scikit-learn` design patterns, specifically **Pipelines** and **ColumnTransformers**, ensuring a clean workflow that seamlessly handles:
1. One-Hot Encoding for categorical data (`Sex`, `Embarked`, `Title`, `Pclass`, `Is_alone`).
2. Standard Scaling for numerical features (`Age`, `Fare`, `Family_size`).
3. Streamlined model fitting and validation.

---

## 📋 How to Run the Project
1. Clone this repository:
```bash
   git clone [https://github.com/yourusername/titanic-survival-prediction.git](https://github.com/yourusername/titanic-survival-prediction.git)