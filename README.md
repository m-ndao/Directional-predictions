# 📈 Directional Prediction of Stock Indexes: DJIA vs. Russell 2000

This project analyzes and forecasts the **directional movement** (up/down) of two major U.S. stock indexes — the **Dow Jones Industrial Average (DJIA)** and the **Russell 2000 (RUT)** — using **econometric models** (Logit, Probit) and **machine learning algorithms** (Random Forest, SVM). The goal is to evaluate model accuracy and build a trading strategy based on forecasted trends.

---

## 🧠 Project Summary

- **Time Period**: February 1999 – December 2019  
- **Target Variables**:
  - `dji` = 1 if DJIA return is positive, 0 otherwise
  - `rti` = 1 if RUT return is positive, 0 otherwise
- **Approaches Used**:
  - Econometric Models: Logistic Regression, Probit Regression (with and without lag terms)
  - Machine Learning: Random Forest (basic and depth-based), Support Vector Machine (SVM)
- **Outcome**: Suggested trading strategy using directional forecasts and macroeconomic indicators.

---

## 🧾 Table of Contents

- [Project Summary](#project-summary)
- [Folder Structure](#folder-structure)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Key Findings](#key-findings)
- [Investment Strategy](#investment-strategy)
- [License](#license)

---

## 📂 Folder Structure

```bash
DJIA_RUT_Directional_Prediction/
│
├── data/                   # Raw and processed datasets
│   ├── raw_data.csv
│   └── processed_data.csv
│
├── notebooks/              # Step-by-step analysis in Jupyter
│   ├── 01_data_exploration.ipynb
│   ├── 02_logit_probit_models.ipynb
│   ├── 03_machine_learning_models.ipynb
│   └── 04_strategy_simulation.ipynb
│
├── models/                 # Trained model artifacts
│   ├── random_forest_dji.pkl
│   └── svm_dji.pkl
│
├── results/                # Model predictions and scores
│   ├── predictions_dji.csv
│   └── accuracy_scores.json
│
├── src/                    # Source code
│   ├── preprocess.py
│   ├── train_models.py
│   └── utils.py
│
├── reports/
│   └── final_report.pdf    # Executive summary with charts
│
├── README.md
└── requirements.txt
