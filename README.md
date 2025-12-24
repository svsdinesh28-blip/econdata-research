📈 S&P 500 Stock Prediction with Explainable AI (XAI)

This project implements an end-to-end machine learning pipeline for predicting next-day stock returns across the S&P 500 universe, combined with Explainable AI (XAI) techniques to interpret model decisions at both global and local levels.

The goal is not just prediction, but transparent, interpretable financial modeling.

🔍 Project Overview

Universe: ~500 S&P 500 stocks (5 years of daily data)

Task: Next-day return prediction

Models: Ensemble of tree-based regressors

Explainability: SHAP + Glass-box Decision Tree

Evaluation: RMSE, portfolio backtest, Sharpe Ratio, Max Drawdown

Reproducibility: Fully reproducible via public dataset

🧠 Methodology
1️⃣ Feature Engineering

Each stock is transformed into a rich feature set combining:

Physics-inspired features

Velocity (price change)

Acceleration (change of velocity)

Momentum

Force (price × volume)

Technical indicators

SMA / EMA (short & long)

RSI

MACD + signal

Bollinger Bands

OBV

Target

Next-day return (t+1)

2️⃣ Predictive Modeling

An ensemble regression model is trained per stock:

XGBoost Regressor

LightGBM Regressor

Random Forest Regressor

Predictions are averaged to reduce variance and improve robustness.

Metrics per stock:

RMSE (out-of-sample)

Predicted next-day return

Buy / Sell signal

3️⃣ Portfolio Construction & Backtesting

Select Top-5 stocks with highest predicted next-day returns

Equal-weighted strategy

Fully invested (daily rebalancing)

Reported metrics

Cumulative return

Sharpe Ratio

Maximum Drawdown

⚠️ Results reflect a research backtest and are not investment advice.

🔎 Explainable AI (XAI)

To ensure interpretability, the project includes two complementary XAI approaches:

🔹 Global Explainability (SHAP)

Feature importance across the full dataset

Identifies dominant drivers such as momentum, MACD, RSI, and velocity

Reveals regime-dependent behavior

🔹 Glass-box Model (Ante-hoc)

Interpretable Decision Tree trained on a directional transformation of returns

Avoids degeneracy caused by near-zero regression targets

Visualizes clear decision rules

🔹 Local Explainability

Feature-level contribution for individual predictions

Shows positive vs negative influences, feature values, and prediction ranges

📊 Outputs

The notebook produces:

✅ Top-5 predicted next-day stocks

✅ RMSE per stock

✅ Buy / Sell signals

✅ Portfolio backtest curve

✅ Sharpe Ratio & Max Drawdown

✅ SHAP summary plot

✅ SHAP local explanation

✅ Interpretable Decision Tree
⚠️ Disclaimer

This project is for educational and research purposes only.
It does not constitute financial or investment advice.

Markets are stochastic, non-stationary, and subject to risk.
✨ Key Takeaways

Ensemble models improve robustness over single predictors

Explainability is essential in financial ML

Directional transformations are critical for meaningful XAI on return data

Transparent models build trust, not just accuracy

for research uses heres my research paper on this topic on SSRN -  https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5674505
