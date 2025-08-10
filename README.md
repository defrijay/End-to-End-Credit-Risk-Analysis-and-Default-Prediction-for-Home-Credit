# **End-to-End Credit Risk Analysis and Default Prediction for Home Credit**

This project implements a comprehensive credit risk analysis process, from data exploration and feature engineering to machine learning modeling to predict potential defaults. The goal is to improve the accuracy of the loan approval process and reduce losses due to credit issues.

## 📌 Project Overview

This project is part of a **Data Analyst & Data Scientist portfolio**, using the Kaggle dataset [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk/overview). The goal is to analyze, model, and deliver actionable business insights to improve loan approval decisions and reduce default risk.

---

## 🎯 Business Problem

Many loan applicants lack a strong traditional credit history, putting them at risk of being rejected or offered less favorable loan terms. Home Credit strives to:

1. Accurately identify borrowers with a high risk of default, while
2. Expanding financial inclusion by approving safe and viable applicants even without a traditional credit history, using alternative data such as external scores, transaction history, and payment behavior.
3. Structuring loans (amount, term, interest rate) that minimizes the risk of default while supporting successful repayment.

**Key Business Questions:**

* Who is likely to default on their loans, and who might be unfairly rejected due to lack of traditional credit history?
* Which features, including alternative data sources, most strongly predict default or repayment capability?
* How can we set underwriting rules that balance approval rate, financial inclusion, and credit risk?

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

## 👤 Author

*Defrizal Yahdiyan Risyad*

[LinkedIn](https://www.linkedin.com/in/defrizalyr?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BqZ%2B7dZzhS%2FCtdV82zspJFQ%3D%3D) | [GitHub](https://github.com/defrijay)

