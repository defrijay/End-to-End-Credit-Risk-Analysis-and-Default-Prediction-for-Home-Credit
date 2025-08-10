# **End-to-End Credit Risk Analysis and Default Prediction for Home Credit**

This project implements a comprehensive credit risk analysis process, from data exploration and feature engineering to machine learning modeling to predict potential defaults. The goal is to improve the accuracy of the loan approval process and reduce losses due to credit issues.

## 📌 Project Overview

This project is part of a **Data Analyst & Data Scientist portfolio**, using the Kaggle dataset [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk/overview). The goal is to analyze, model, and deliver actionable business insights to improve loan approval decisions and reduce default risk.

---

## 🎯 Business Problem

Many applicants lack sufficient credit history, leading to either rejection or unfavorable loan terms. Home Credit aims to:

1. Identify high-risk borrowers.
2. Expand financial inclusion by approving safe applicants without traditional credit history.
3. Suggest loan structures (amount, term, interest) that minimize risk.

**Key Business Questions:**

* Who is likely to default on their loans?
* Which features most strongly predict default?
* How can we set underwriting rules to balance approval rate and risk?

---

## 📊 Dataset Description

**Main files:**

* `application_train.csv` / `application_test.csv`: Main application data.
* `bureau.csv` / `bureau_balance.csv`: Previous credit history from other institutions.
* `previous_application.csv`: Historical Home Credit applications.
* `installments_payments.csv`: Repayment history.
* `pos_cash_balance.csv` / `credit_card_balance.csv`: Loan and credit card history.
* `HomeCredit_columns_description.csv`: Feature documentation.

---

## 🛠 Methodology

1. **Data Understanding & Cleaning**

   * Merge datasets using keys (`SK_ID_CURR`, `SK_ID_BUREAU`, `SK_ID_PREV`).
   * Handle missing values, duplicates, and data types.

2. **Exploratory Data Analysis (EDA)**

   * Target distribution, feature distributions, missingness heatmap.
   * Relationship between features and default rates.

3. **Feature Engineering**

   * Aggregate credit history, repayment ratios, delinquency counts.
   * Create time-based features (employment length, credit age).
   * Encode categorical variables.

4. **Modeling**

   * Baseline: Logistic Regression.
   * Advanced: Random Forest, LightGBM, XGBoost, Stacking.
   * Evaluate with AUC, Precision, Recall, Calibration.

5. **Explainability & Fairness**

   * SHAP values for feature importance.
   * Bias checks by gender and region.

6. **Deployment & Monitoring**

   * Export model, create scoring API.
   * Monitor drift, AUC decay, PSI.

---

## 📈 Key Metrics

* **Primary:** AUC
* **Secondary:** Precision, Recall, Brier Score, Lift\@k, KS-statistic.
* **Business Impact:** Reduction in default rate, approval rate increase, expected loss reduction.

---

## 📂 Project Structure

```
HomeCredit_DefaultRisk/
│
├── data/                  # Raw & processed datasets
├── notebooks/             # Jupyter notebooks for EDA, modeling
├── scripts/               # Python scripts for data prep, modeling
├── models/                # Saved model artifacts
├── reports/               # PDF/slide business insights
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

---

## 🚀 How to Run

```bash
# 1. Clone repo
git clone <repo-url>
cd HomeCredit_DefaultRisk

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run notebooks
jupyter notebook
```

---

## 📎 Deliverables

* **EDA & Modeling Notebook**: Full analysis, feature engineering, and modeling.
* **Insight Deck**: 17-slide business presentation.
* **Model Artifacts**: Pickle/Joblib files.
* **README.md**: Documentation.

---

## 👤 Author

*Defrizal Yahdiyan Risyad*

[LinkedIn](#https://www.linkedin.com/in/defrizalyr?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BqZ%2B7dZzhS%2FCtdV82zspJFQ%3D%3D) | [GitHub](#https://github.com/defrijay)
