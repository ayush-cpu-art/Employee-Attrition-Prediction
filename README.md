# 👥 Employee Attrition Prediction

A machine learning classification project that predicts employee attrition using Decision Tree and Random Forest classifiers on the IBM HR Analytics Employee Attrition dataset.

## 🎯 Objective

The objective of this project is to predict whether an employee is likely to leave the organization and compare the performance of Decision Tree and Random Forest classification models.

## 📊 Dataset

**IBM HR Analytics Employee Attrition & Performance Dataset**

The dataset contains **1,470 employee records** with **35 original features** related to employee demographics, job characteristics, compensation, satisfaction, and other HR attributes.

### Target Variable

`Attrition`

| Value | Meaning |
|---|---|
| `Yes` | Employee left the organization |
| `No` | Employee stayed |

The dataset contains:

- 1,233 employees who did not leave
- 237 employees who left

This class imbalance makes metrics such as Precision, Recall, and F1-Score important when evaluating the models.

## 🛠️ Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## ⚙️ Methodology

1. Load the IBM HR Analytics dataset.
2. Perform exploratory data understanding.
3. Check for missing values.
4. Remove constant and identifier columns.
5. Encode categorical variables.
6. Split the dataset using an 80/20 stratified train-test split.
7. Train Decision Tree and Random Forest classifiers.
8. Evaluate both models using Accuracy, Precision, Recall, and F1-Score.
9. Analyze confusion matrices.
10. Visualize Random Forest feature importance.

## 🤖 Models

### Decision Tree

A Decision Tree classifier was trained to predict employee attrition based on the available HR features.

### Random Forest

A Random Forest classifier was trained using multiple decision trees to improve predictive performance and reduce dependence on a single tree.

## 📈 Model Comparison

| Metric | Decision Tree | Random Forest |
|---|---:|---:|
| Accuracy | **78.23%** | **84.35%** |
| Precision | **31.91%** | **54.55%** |
| Recall | **31.91%** | **12.77%** |
| F1-Score | **31.91%** | **20.69%** |

## 🔍 Observations

- Random Forest achieved higher overall **accuracy (84.35%)** and **precision (54.55%)**.
- Decision Tree achieved higher **recall (31.91%)** and **F1-score (31.91%)**.
- The dataset contains substantially more employees who did not leave than employees who left.
- Because of this class imbalance, accuracy alone is not sufficient for evaluating attrition prediction.
- Confusion matrices provide additional insight into how the models identify employees who experienced attrition.
- Random Forest feature importance was used to identify features that contributed most to its predictions.

## 📁 Project Structure

```text
Employee-Attrition-Prediction/
├── images/
├── .gitignore
├── employee_attrition_prediction.ipynb
├── README.md
├── requirements.txt
└── WA_Fn-UseC_-HR-Employee-Attrition.csv