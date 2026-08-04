# Telecom Customer Churn Prediction Using Machine Learning

A machine learning project that analyzes telecom customer data to predict which
customers are likely to churn (leave for a competitor), identify the key
drivers behind churn, and surface actionable retention insights through an
interactive Power BI dashboard.

---

## Table of Contents
- [Problem Statement](#problem-statement)
- [Objective](#objective)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Usage Instructions](#usage-instructions)
- [Running the Project](#running-the-project)
- [Future Improvements](#future-improvements)

---

## Problem Statement

Customer churn is one of the most expensive problems telecom providers face —
acquiring a new customer typically costs far more than retaining an existing
one. Without a way to flag at-risk customers early, retention teams end up
reacting after a customer has already decided to leave, rather than
intervening in time. This project builds a predictive model that scores
customers on churn risk and surfaces the specific behavioral and contractual
factors driving that risk, so retention efforts can be targeted rather than
generic.

---

## Objective

- Build a binary classification model to predict whether a customer will churn.
- Identify which features (contract type, tenure, billing method, service
  usage, etc.) contribute most to churn risk.
- Translate model output into a business-facing Power BI dashboard that
  non-technical stakeholders can use to spot at-risk segments.

---

## Dataset

The dataset includes customer-level attributes across four categories:

1. **Demographics** — gender, senior citizen status, partner/dependents.
2. **Account Information** — tenure, contract type, paperless billing, payment method.
3. **Services Subscribed** — phone service, internet service, online security,
   tech support, streaming TV/movies, device protection.
4. **Billing** — monthly charges, total charges.
5. **Target Variable** — `Churn` (Yes/No).

---

## Methodology

1. **Data Cleaning & Preprocessing**
   Handled missing values, corrected data types, and encoded categorical
   features for modeling.

2. **Exploratory Data Analysis (EDA)**
   Examined churn distribution across contract types, tenure bands, payment
   methods, and service subscriptions to surface early patterns.

3. **Feature Engineering**
   Derived features (e.g., tenure buckets, total services subscribed) to
   improve model signal beyond the raw columns.

4. **Model Training & Evaluation**
   Trained and compared classification models (Logistic Regression, Random
   Forest, and Gradient Boosting variants), evaluating on accuracy, precision,
   recall, and ROC-AUC — with attention to the class imbalance in the churn
   label.

5. **Dashboard Development**
   Connected model outputs and key EDA findings to a Power BI dashboard for
   churn trends, customer segmentation, and predictor importance.

---

## Key Findings

- Certain contract types and billing methods are associated with
  disproportionately higher churn rates.
- Tenure is one of the strongest predictors — newer customers churn at a
  noticeably higher rate than long-tenured ones.
- Customers without add-on services (e.g., tech support, online security)
  show higher churn propensity, suggesting these services may increase
  stickiness.

*(Update this section with your own model's specific numbers once finalized —
e.g., best model + accuracy/ROC-AUC score, and the top 3–5 features by
importance.)*

---

## Tech Stack

- **Language:** Python (Pandas, NumPy, Scikit-learn, Matplotlib/Seaborn)
- **Visualization:** Power BI
- **Notebook Environment:** Jupyter

---

## Project Structure

```
Telecom-Customer-Churn-Prediction-Using-Machine-Learning/
├── data/                  # Raw and processed dataset
├── notebooks/             # EDA, feature engineering, modeling notebooks
├── powerbi/               # Power BI dashboard (.pbix)
├── requirements.txt
└── README.md
```

*(Adjust this to match your actual folder layout.)*

---

## Usage Instructions

```bash
# Clone the repository
git clone https://github.com/shdbfrz/Telecom-Customer-Churn-Prediction-Using-Machine-Learning.git
cd Telecom-Customer-Churn-Prediction-Using-Machine-Learning

# Install dependencies
pip install -r requirements.txt
```

## Running the Project

1. Open the notebook(s) in the `notebooks/` folder in Jupyter.
2. Run cells in order: data loading → EDA → feature engineering → modeling.
3. Open the `.pbix` file in Power BI Desktop to explore the interactive dashboard.

---

## Future Improvements

- Deploy the trained model behind a simple Flask/FastAPI endpoint for
  real-time churn scoring.
- Add SHAP-based explainability to make individual predictions interpretable
  for business stakeholders.
- Experiment with XGBoost/LightGBM for a potential accuracy uplift.

---

### Author

**Shadab Firoz** — [GitHub](https://github.com/shdbfrz) · [LinkedIn](https://linkedin.com/in/shadab-firoz-38031a30b)
