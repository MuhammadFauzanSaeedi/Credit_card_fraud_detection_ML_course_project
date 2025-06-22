# 💳 Credit Card Fraud Detection using Machine Learning

This project applies both **supervised** and **unsupervised** machine learning techniques to detect fraudulent credit card transactions. It includes full data preprocessing, exploratory data analysis (EDA), model building (Decision Tree, XGBoost), unsupervised clustering (K-Means), and interpretation of results. This project was developed as part of a machine learning learning program and showcases a complete data analytics workflow, from data cleaning to model deployment, using real-world credit card fraud data.

---

## 📊 Dataset Overview

The dataset includes transaction-level details such as:
- Date and time
- Customer location and merchant info
- Transaction amount
- Customer demographics
- Target label: `is_fraud` (0 = legitimate, 1 = fraudulent)

---

## 📁 Tasks Breakdown

### ✅ Task 1 – Data Cleaning & EDA
- Handled missing values
- Engineered features: transaction hour, day, customer age
- Encoded high- and low-cardinality categorical variables
- Performed correlation analysis and visualized fraud patterns

### ✅ Task 2 – Modeling
- Trained and evaluated:
  - `DecisionTreeClassifier`
  - `XGBoostClassifier`
  - `KMeans` clustering with PCA visualization
- Evaluated using:
  - Accuracy, Precision, Recall, F1-score
  - Confusion Matrix
  - ROC-AUC (for XGBoost)
  - Elbow method (Inertia WCSS) (for K-Means)

---

## 📈 Results Summary

| Model         | Accuracy | Fraud Recall | Precision | F1-score | ROC-AUC |
|---------------|----------|--------------|-----------|----------|---------|
| Decision Tree | 96%      | 95%          | 13%       | 22%      | 0.98    |
| XGBoost       | **99%**  | **96%**      | 30%       | 46%      | **0.998** |
| K-Means       | —        | —            | —         | —        | —       |

- **XGBoost outperformed** in recall and ROC-AUC, making it the best choice for production.
- **K-Means**, though unsupervised, naturally separated fraud into its own cluster.
- **Decision Tree** offered high interpretability but lower fraud precision.

---

## 💼 Business Recommendations

1. ✅ **Deploy XGBoost** for real-time fraud detection with high sensitivity.
2. ⚠️ Use a **manual review process** for flagged transactions due to false positives.
3. 🔍 Apply **K-Means clustering** periodically to discover emerging fraud patterns.
4. 🔁 **Retrain models monthly** to adapt to evolving fraud tactics.
5. 📢 Implement **customer alert systems** for flagged transactions.
6. 📈 Monitor top fraud indicators like transaction amount, time, location deviation.

---

## 🛠 Tech Stack

- Python 3
- Jupyter Notebook
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- PCA for dimensionality reduction

---

### 📥 Dataset Download

> [Click here to download the full dataset](https://drive.google.com/file/d/12dwKbLYE-jhOtxsPVWO6ZP-_1oCtEzjf/view?usp=drive_link)
