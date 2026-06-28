# Cross-Channel Promotional Budget Optimization — Task 5

## 📌 Architectural Overview
This module applies a continuous **Linear Regression Optimization Architecture** to model product sales outcomes based on historical cross-channel promotional capital allocations across TV, Radio, and Newspaper channels.

## 🛠️ Production Engineering Workflow
1. **Matrix Structural Cleanup**: Eliminated unneeded structural index padding arrays from `Advertising.csv` during initial storage ingestion to preserve cross-validation data integrity.
2. **Multi-Collinearity Diagnostics**: Constructed correlation matrices via `Seaborn` heatmaps to mathematically map separate variable dependencies before model execution.
3. **Linear Fitting**: Implemented a continuous `LinearRegression` model to solve the hyper-plane equations and compute specific platform multipliers (coefficients).
4. **Diagnostic Metrics**: Evaluated general predictive drift metrics using Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE).

## 📊 Commercial Strategic Value
The computed model coefficients serve as precise return-on-investment (ROI) multipliers. This mathematical clarity enables enterprise management to run automated "what-if" budget allocation scenarios and secure optimized sales targets before committing capital.

