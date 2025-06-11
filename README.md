# STUDENT-PERFORMANCE
# 🎓 Student Pass/Fail Prediction using Machine Learning

This project predicts whether a student will **pass or fail** based on their academic and demographic features. We use machine learning algorithms to perform binary classification on the [Student Performance Dataset](https://archive.ics.uci.edu/ml/datasets/Student+Performance).

---

## 📂 Dataset

- File: `student-mat.csv`
- Source: UCI Machine Learning Repository
- Target column: `G3` (Final Grade), which we converted into a binary variable:
  - `Pass = 1` if G3 ≥ 10
  - `Fail = 0` if G3 < 10

---

## 🔍 Project Steps

1. **Data Preprocessing**
   - Loaded the dataset using pandas
   - Handled missing values (none found)
   - Encoded categorical variables using `pd.get_dummies()`

2. **Feature Selection**
   - Used correlation analysis to select features highly related to `G3`
   - Selected top correlated features for model input

3. **Created Binary Target**
   - Created a new column `'Pass'` from `G3`
   - Dropped `G3` since it's no longer needed

4. **Model Training**
   - Split the data into training and test sets (80/20)
   - Trained two models:
     - **Logistic Regression**
     - **Decision Tree Classifier**

5. **Evaluation**
   - Used:
     - Accuracy
     - F1-Score
     - Confusion Matrix

---

## 🧠 Model Comparison

| Metric              | Logistic Regression | Decision Tree |
|---------------------|---------------------|----------------|
| Accuracy            | ✅ **89.9%**         | 88.6%          |
| F1-score (Pass)     | ✅ **0.92**          | 0.91           |
| Precision (Pass)    | ✅ 0.94              | 0.92           |

✅ **Final Choice**: **Logistic Regression** is the better model for this task due to its higher accuracy and F1-score.

---

## 🧰 Tech Stack

- Python
- Jupyter Notebook
- pandas, numpy
- scikit-learn
- seaborn, matplotlib

---

## 📁 Folder Structure

