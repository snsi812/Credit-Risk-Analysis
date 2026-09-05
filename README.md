# 📊 End-to-End Credit Risk Analysis
### Score Generation, Risk Classification & Approval Engine

A data analytics pipeline that predicts credit default risk, generates a 300–900 credit score for every applicant, and automates the approval decision — built using Python, SQL, Excel, and Power BI.

---

## 🎯 Overview

Banks face a trade-off: approve a risky applicant and risk financial loss, or reject a safe one and lose revenue. This project solves that by analysing applicant data, predicting default probability with machine learning, converting it into a credit score, and automatically classifying each applicant as **Approved**, **Under Review**, or **Rejected** — visualised in an interactive Power BI dashboard.

---

## 🧱 Pipeline

```
Raw Data → Cleaning & Feature Engineering → ML Model →
Credit Score → SQL Decision Engine → Excel Analysis → Power BI Dashboard
```

## 🛠️ Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=power-bi&logoColor=black)

Python (preprocessing + ML) → SQL (decision logic) → Excel (exploration) → Power BI (dashboard)

---

## 📂 Dataset

[Credit Risk Dataset — Kaggle](https://www.kaggle.com/datasets/laotse/credit-risk-dataset). Not included here due to size — download and place in `data/`.

---

## 🤖 Model Results

| Model | Accuracy | AUC Score |
|---|---|---|
| Logistic Regression (baseline) | ~80–85% | ~0.85 |
| **Random Forest (final)** ✅ | **~88–92%** | **~0.94–0.96** |

**Credit Score Formula:**
```
Credit Score = 300 + (Probability of NOT Defaulting × 600)
```

| Score | Category | Decision |
|---|---|---|
| 800–900 | Very Safe | Approved |
| 700–799 | Safe | Approved |
| 600–699 | Moderate Risk | Review |
| 300–599 | High Risk | Rejected |

---

## 📊 Power BI Dashboard

Four visuals — Total Applicants (KPI), Decision Split (Donut), Risk Breakdown (Stacked Bar), Employment vs Credit Score (Line) — with slicers for Risk Category and Decision.

![Dashboard Preview](images/dashboard_screenshot.png)

---

## 📁 Repository Structure

```
credit-risk-analysis/
├── notebooks/       → Python preprocessing & model training
├── sql/             → Decision engine queries
├── excel/           → Pivot tables & charts
├── dashboard/       → Power BI file + screenshot
├── reports/         → Project documentation (PDF)
└── data/            → Data dictionary (raw CSV not included)
```

---

## 🚀 How to Run

1. Download the dataset from Kaggle → place in `data/`
2. Run `notebooks/01_preprocessing_colab.ipynb` → produces `cleaned_data.csv`
3. Run `notebooks/02_model_colab.ipynb` → produces `scored_applicants.csv`
4. Import scored CSV into DB Browser for SQLite → run `sql/queries_v2.sql`
5. Open `dashboard/dashboard.pbix` in Power BI Desktop

---

## 👤 Author

**Sanskar Gupta** — B.E. Information Technology, UIET, Panjab University, Chandigarh
