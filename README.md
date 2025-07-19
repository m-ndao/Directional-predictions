# 📈 Directional Prediction of Stock Indexes: DJIA vs. Russell 2000 Using Econometric and Machine Learning Models

This project investigates the **directional forecasting** (up/down movement) of two major stock indices — **Dow Jones Industrial Average (DJIA)** and **Russell 2000 (RUT)** — using **Logit/Probit regression** and **machine learning models** such as **Random Forest** and **Support Vector Machines (SVM)**.


---

## 📌 Project Overview

- **Timeframe**: February 1999 – December 2019  
- **Goal**: Predict whether the DJIA or RUT index will go up or down in the next quarter using macroeconomic variables.
- **Models Used**:
  - Logistic & Probit Regressions (autoregressive and simple)
  - Random Forest Classifier
  - Support Vector Machine (SVM)

- **Evaluation Metrics**: 
  - Test Accuracy
  - Cross-Validation Accuracy
  - Confusion Matrix
  - Feature Importance
  - Strategy Simulation

---
## 📁 Project Structure

```bash
DJIA_RUT_Directional_Prediction/
│
├── data/                   # Raw and processed datasets
├── notebooks/              # Step-by-step Jupyter notebooks
│   ├── 01_data_exploration.ipynb
│   ├── 02_logit_probit_models.ipynb
│   ├── 03_machine_learning_models.ipynb
│   └── 04_strategy_simulation.ipynb
├── models/                 # Saved trained models (joblib/pickle)
├── results/                # Predictions, performance scores
├── reports/                # Final report, visualizations
├── src/                    # Python scripts for modular execution
├── requirements.txt
└── README.md
🔑 Key Results
Model	DJIA Accuracy (Test)	DJIA CV Accuracy	RUT Accuracy (Test)	RUT CV Accuracy
Logit/Probit (Auto)	72%	62%	66%	63%
Logit/Probit + Recession	65%	↓ from 67%	≈ no change	≈ no change
Random Forest (w/ Rec.)	71%	53%	71%	49%
Random Forest (no Rec.)	61%	53%	65%	50%
SVM (w/ Rec.)	69%	60%	71%	61%
SVM (no Rec.)	62%	60%	61%	61%

📌 Observation: While test accuracy was relatively high, most models showed signs of overfitting, especially Random Forest when evaluated with cross-validation.

💸 Investment Strategy
Based on model forecasts and findings from the financial literature, the following multi-step investment strategy is proposed:

Buy the RUT index when a positive signal is forecasted.

Hold for up to 3 quarters.

Sell when negative predictions appear between quarters 3–4.

Switch to DJIA after selling RUT.

Hold for 1 full year based on its long-term predictability.

Use quarterly forecast updates to decide reallocations.

🧠 Chen et al. (2006) Extension:

Buy newly added RUT stocks on the last trading day of May.

Sell deleted RUT stocks on the last trading day of August.
This method helps reduce exposure to tracker error and anticipates short-term excess returns.

🧠 Discussion & Evaluation
Overfitting was a major concern. While many models performed well on the test set, their cross-validation accuracy dropped significantly, especially for Random Forest.

The recession indicator boosted performance in machine learning models but reduced performance in econometric ones.

For example, including it improved Random Forest DJIA accuracy from 61% to 71%, but reduced Logit accuracy from 67% to 65%.

Contrary to Ballings et al. (2015), Random Forest was the weakest performer due to a lack of hyperparameter tuning (e.g., tree depth).

Support Vector Machines and Logit models showed comparable and stable results around 61–62% for both indexes.

Market Insights:

RUT has higher short-term returns but also greater volatility.

DJIA provides more consistent long-term gains.

✅ Conclusion
This study compared econometric and machine learning models for forecasting the directional returns of the DJIA and RUT indexes. Key takeaways include:

Econometric models (Logit/Probit) offer moderate and reliable accuracy (~62%).

Support Vector Machines perform comparably to logit models and generalize better than Random Forests.

RUT is a more profitable short-term investment, while DJIA is better suited for long-term strategies.

Cross-validation was critical in uncovering overfitting across models.

🔧 Recommendations
Use cross-validation consistently when evaluating forecasting models.

Tune random forest tree depth and number of estimators to improve generalization (as suggested by Wang, 2022).

Explore K-Nearest Neighbors and Neural Networks as alternative classifiers.

Extend the strategy simulation to real trading costs and slippage.

Apply rolling windows or walk-forward validation to simulate real-time model updates.

📚 References
Alvarez-Díaz, M., Caballero, M. A., & Leiva, J. C. (2014). Forecasting stock prices using logistic regression.

Ballings, M., Van den Poel, D., Hespeels, N., & Gryp, R. (2015). Evaluating multiple classifiers for financial market direction forecasting.

Chen, H., Noronha, G., & Singal, V. (2006). Index Changes and Losses to Index Fund Investors.

Nyberg, H. (2011). Forecasting U.S. recessions with dynamic binary response models.

Qian, B., & Rasheed, K. (2007). Stock market prediction with multiple classifiers.

Wang, H. (2022). The influence of decision tree depth on random forest forecasting accuracy.

