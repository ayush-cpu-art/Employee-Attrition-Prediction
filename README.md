# Employee Attrition Prediction

A machine learning classification project that predicts whether an employee is likely to leave an organization using HR analytics data.

The project explores employee-related features, performs preprocessing and exploratory analysis, and compares Decision Tree and Random Forest classifiers using multiple evaluation metrics.

---

## 📌 Overview

Employee attrition can affect productivity, recruitment costs, and workforce stability.

This project uses historical HR data to build classification models that predict employee attrition based on factors such as:

- Age
- Job satisfaction
- Monthly income
- Job level
- Work-life balance
- Overtime
- Distance from home
- Years at company
- Job role
- Environment satisfaction
- And other employee-related attributes

The project focuses on understanding the data, preparing it for machine learning, training classification models, and evaluating their performance.

---

## 🎯 Problem Statement

Build a machine learning model that predicts whether an employee will leave the organization based on available HR attributes.

**Target variable:** `Attrition`

- `0` → No
- `1` → Yes

---

## 📊 Dataset

The project uses the IBM HR Analytics Employee Attrition dataset.

### Dataset characteristics

- **Records:** 1,470
- **Original features:** 35
- **Target:** Attrition
- **Missing values:** None

### Class distribution

| Attrition | Count |
|-----------|------:|
| No | 1,233 |
| Yes | 237 |

The dataset is imbalanced, with substantially more employees who did not leave than employees who did.

Therefore, accuracy is considered alongside precision, recall, and F1-score.

---

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Inspected dataset structure and statistics.
3. Checked for missing values.
4. Removed constant or unnecessary columns:
   - `EmployeeCount`
   - `EmployeeNumber`
   - `Over18`
   - `StandardHours`
5. Encoded categorical variables using `LabelEncoder`.
6. Separated features and target variable.
7. Split the data into training and testing sets using an 80/20 stratified split.

### Final dataset

After removing the unnecessary columns:

- **Features:** 30
- **Target:** Attrition

---

## 🤖 Machine Learning Models

Two classification algorithms were implemented:

### 1. Decision Tree Classifier

A single decision tree was trained using:

```python
DecisionTreeClassifier(random_state=42)
