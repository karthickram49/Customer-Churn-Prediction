# Customer-Churn-Prediction
An end-to-end Machine Learning pipeline built in Python to predict customer churn using the Telco customer churn dataset, featuring exploratory data analysis, class imbalance handling, and multi-model classification comparison.  


# Customer Churn Prediction Pipeline

An end-to-end Machine Learning project built in Python to predict customer churn using the Telco customer churn dataset. The pipeline covers data cleaning, exploratory data analysis (EDA), handling class imbalance via SMOTE, and model evaluation using 5-fold cross-validation.

---

## 📌 Project Overview

Customer churn is a critical business metric in the telecommunications industry. The goal of this project is to build a classification pipeline that accurately identifies customers at risk of leaving, enabling business teams to execute targeted retention strategies and mitigate revenue loss.

---

## 🛠️ Data Pipeline & Workflow

1. **Data Cleaning & Preparation:**
   * Removed non-predictive identifiers (`customerID`).
   * Cleaned hidden whitespace characters in `TotalCharges` and converted the column to `float64`.
   * Verified data integrity and handled zero-value edge cases.

2. **Exploratory Data Analysis (EDA):**
   * Analyzed numerical feature distributions (`tenure`, `MonthlyCharges`, `TotalCharges`) using histograms and KDE plots.
   * Inspected feature ranges and potential outliers using box plots.
   * Checked categorical feature distributions using count plots.
   * Highlighted target class imbalance (`Churn`: ~73% retained vs. ~27% churned).

3. **Preprocessing & Class Imbalance:**
   * Mapped binary target variable (`Churn`: `Yes` $\rightarrow$ 1, `No` $\rightarrow$ 0).
   * Split data into 80% training and 20% test sets.
   * Applied **SMOTE (Synthetic Minority Over-sampling Technique)** strictly on the training dataset to resolve class imbalance without data leakage.

4. **Model Training & Evaluation:**
   * Trained and evaluated multiple classifiers using **5-Fold Cross-Validation**:
     * **Decision Tree**
     * **XGBoost**
     * **Random Forest**

---

## 📊 Results & Performance

| Model | 5-Fold Cross-Validation Accuracy |
| :--- | :--- |
| **Random Forest** | **84%** |
| XGBoost | 83% |
| Decision Tree | 78% |

* **Top Performing Model:** Random Forest achieved the highest average cross-validation accuracy (**84%**), demonstrating strong generalization across unseen folds.

---

## 💻 Tech Stack

* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, XGBoost, Imbalanced-Learn (`imblearn`)
* **Environment:** Jupyter Notebook / Google Colab

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/customer-churn-prediction.git](https://github.com/your-username/customer-churn-prediction.git)
   cd customer-churn-prediction
