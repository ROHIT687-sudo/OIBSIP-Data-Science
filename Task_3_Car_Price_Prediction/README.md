# Supervised Asset Valuation & Appraisal Engine — Task 3

## 📌 Architectural Overview
This directory implements a continuous **Regression Architecture with Feature Engineering** to automate the asset valuation of secondary-market vehicles. The model establishes statistical weights across mixed feature sets—including odometer metrics, mechanical parameters, and temporal depreciation indices—to output accurate sales values.

## 🛠️ Production Engineering Workflow
1. **Derived Feature Engineering**: Converted static manufacturing calendar variables into an actionable continuous temporal indicator: `Car_Age` (derived relative to the 2026 operational year), capturing mathematical depreciation vectors.
2. **Mixed Column Transformer Pipeline**: Implemented an automated preprocessing pipeline utilizing `ColumnTransformer` to handle dual-type data inputs simultaneously. Numeric metrics are passed through while categorical strings (`Fuel_Type`, `Transmission`, `Selling_type`) are vectorized via `OneHotEncoder`.
3. **Predictive Analytics**: Deployed a high-capacity `RandomForestRegressor` to capture non-linear depreciation patterns across mixed data spaces.
4. **Data Leakage Mitigation**: Encapsulated all transformation rules and estimators within a unified Scikit-Learn `Pipeline`, securing deterministic inference behaviors across development, testing, and production phases.

## 📉 Diagnostic Evaluation Metrics
* **Baseline Accuracy Indicator**: R² Score (Coefficient of Determination)
* **Error Tracking**: Mean Absolute Error (MAE) computing the absolute average pricing variance in Lakhs.

