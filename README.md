# 📊 Customer Churn Analysis & Prediction

> **End-to-end machine learning project** — predicting telecom customer churn using Random Forest, with an interactive Power BI dashboard for business stakeholders.


---

## 📌 Problem Statement

A telecom company is losing **26.99% of its customers** — amounting to **1,732 churned customers** out of 6,418 total. The business needs to:

1. Understand **why** customers are leaving
2. Identify **which** customers are most at risk
3. Take **proactive action** before they churn

This project builds an ML pipeline that flags high-risk customers and provides visual insights to business teams through Power BI.

---

## 🖥️ Dashboard Preview

### Summary Dashboard — Business Overview
![Churn Analysis Summary Dashboard](dashboard/Power_BI_Summary.png)

### Prediction Dashboard — At-Risk Customers
![Churn Prediction Dashboard](dashboard/Power_BI_Prediction.png)

---

## 🔑 Key Insights

| Insight | Finding |
|---|---|
| Overall churn rate | **26.99%** across 6,418 customers |
| Highest-risk contract | Month-to-month → **46.53% churn** |
| Lowest-risk contract | Two-year → **2.73% churn** |
| Riskiest internet type | Fiber Optic → **41.10% churn** |
| Top churn reason | Competitor offerings (**761 customers**) |
| Gender split (churned) | 64.15% Male, 35.85% Female |
| Predicted at-risk customers | **70 customers** flagged for intervention |

> 💡 **Bottom line**: Contract type is the single strongest predictor of churn. A customer on a month-to-month plan is **17× more likely to churn** than one on a 2-year contract.

---

## 🗺️ Geographic Distribution

Top churning states:
- West Bengal · Maharashtra · Uttar Pradesh · Tamil Nadu · Karnataka · Punjab

---

## 🛠️ Tech Stack

```
Python 3.8+
├── pandas          — data manipulation
├── numpy           — numerical operations
├── matplotlib      — data visualization
├── seaborn         — statistical plots
├── scikit-learn    — Random Forest model
└── joblib          — model serialization

Power BI           — interactive business dashboard
```

---

## 📁 Project Structure

```
customer-churn-analysis/
│
├── 📓 Customer_Churn_Data.ipynb    ← Main ML notebook
│
├── 📁 data/
│   └── churn_data_sample.csv       ← Sample dataset
│
├── 📁 dashboard/
│   ├── Power_BI_Summary.png        ← Business overview
│   └── Power_BI_Prediction.png     ← Prediction results
│
├── 📁 model/
│   └── random_forest_model.pkl     ← Trained model
│
├── 📄 requirements.txt
└── 📄 README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook or Google Colab

### Installation

```bash
# 1. Clone the repository
# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook Customer_Churn_Data.ipynb
```

---

## 🤖 Model Pipeline

```
Raw Data → Data Cleaning → Feature Engineering → Label Encoding
    → Train/Test Split (80/20) → Random Forest (100 estimators)
        → Evaluation → Prediction on New Data → Export (.pkl)
```

### Features Used
- Demographics: `Gender`, `Age`, `Married`, `State`
- Account: `Tenure`, `Contract`, `Payment_Method`, `Monthly_Charge`
- Services: `Internet_Type`, `Online_Security`, `Streaming_TV`, `Unlimited_Data`, and 10 more

### Model Highlights
- **Algorithm**: Random Forest Classifier
- **Estimators**: 100 trees, `random_state=43`
- **Target**: `Customer_Status` → Churned (1) / Stayed (0)
- **Output**: Prediction CSV with at-risk customer profiles

---

## 📊 Service-Level Churn Rates

| Service | Not Subscribed (churn %) | Subscribed (churn %) |
|---|---|---|
| Online Security | 84.6% | 15.4% |
| Premium Support | 83.5% | 16.5% |
| Online Backup | 71.9% | 28.1% |
| Phone Service | 9.4% | **90.6%** |
| Internet Service | 6.3% | **93.7%** |

> Customers **without** security/support add-ons churn at dramatically higher rates — a key upsell opportunity for retention teams.

---

## 📂 Dataset

The dataset contains **6,418 telecom customer records** with 30+ features including:
- Customer demographics (age, gender, state, marital status)
- Account information (tenure, contract type, billing)
- Services subscribed (streaming, security, backup, etc.)
- Churn label and reason

> ⚠️ The full dataset is not included due to size. A sample is available in `/data/`. Request access via the Issues tab.

---

---

---

⭐ **If this project helped you, consider giving it a star!**
