Explainable Machine Learning for Global Inflation Forecasting

This repository contains the code and analysis for the working paper:

Explainable Machine Learning for Global Inflation Forecasting: A Random Forest and Surrogate Tree Approach

The project develops an interpretable machine learning framework to forecast global inflation while preserving economic transparency, using publicly available IMF data.

📌 Motivation

Inflation forecasting is central to macroeconomic policy, yet traditional econometric models often struggle to capture nonlinear global interactions. Modern machine learning models improve predictive accuracy but are frequently criticized for being opaque.
This project bridges that gap by combining a high-performing Random Forest model with an interpretable surrogate decision tree, allowing both accurate prediction and policy-relevant explanation.

📊 Data

Source: IMF Global Inflation Database

Coverage: 190+ countries

Period: 1970–2024

Frequency: Annual (headline CPI inflation)

All data used are publicly available and aggregated at the country level.

🧠 Features Used
Feature	Description
Year	Calendar year
Lag_Inflation	Previous year’s inflation rate (captures persistence)
Regional_Avg_Inflation	Average inflation of regional peers
GDP_Growth	Annual real GDP growth
Interest_Rate	Policy interest rate
Exchange_Rate_Index	Nominal effective exchange rate
⚙️ Methodology

Random Forest Regressor

Captures nonlinear interactions in global inflation dynamics

Achieves strong predictive performance (R² ≈ 0.83)

Global Surrogate Decision Tree

Trained on Random Forest predictions

Provides a transparent, rule-based approximation of the model logic

Enables interpretation of key inflation thresholds and regimes

Explainability Analysis

Feature importance

Decision tree structure

Economic interpretation aligned with macroeconomic theory

📈 Key Results

Random Forest R²: ~0.829

Surrogate Tree Fidelity (R² vs RF): ~0.417

Primary driver: Inflation persistence (lagged inflation)

Secondary drivers: GDP growth, interest rates, exchange rates, regional spillovers

The results confirm that inflation is highly persistent, globally interconnected, and influenced by macroeconomic policy conditions.


📄 Paper

The full working paper is available as a preprint and has been submitted to SSRN:

Explainable Machine Learning for Global Inflation Forecasting:
A Random Forest and Surrogate Tree Approach
(SSRN submission pending public posting)

⚖️ Ethics & Transparency

This study uses publicly available, aggregated macroeconomic data and does not involve human subjects. No ethics approval was required.

📜 License

This repository is intended for academic and educational use.
