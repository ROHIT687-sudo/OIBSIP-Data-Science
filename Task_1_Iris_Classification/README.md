# Multi-Class Taxonomical Classification Architecture — Task 1

## 📌 Architectural Overview
This directory houses a deterministic machine learning pipeline designed to perform **Multi-Class Supervised Classification** on morphometric datasets. The core objective is to map continuous botanical dimensions (sepal and petal lengths/widths) to discrete taxonomic distributions across three species of the Iris genus: *Setosa, Versicolor, and Virginica*.

## 🛠️ Production Engineering Workflow
1. **Feature Ingestion & Isolation**: Parsed the structured `Iris.csv` source, isolated the target vector (`Species`), and decoupled incremental unique identifiers (`Id`) to prevent multi-collinearity or artificial pattern matching.
2. **Variance Normalization**: Implemented `StandardScaler` transformations to compute z-scores across continuous feature spaces. This step ensures coordinate-based distance calculations are not mathematically dominated by features with larger ranges.
3. **Ensemble Modeling**: Deployed a `RandomForestClassifier` initialized with 100 estimator trees to compute optimal non-linear decision boundaries via stratified information gain splits.
4. **Inference Schema Alignment**: Mitigated runtime matrix verification anomalies (`UserWarning: feature names`) by converting raw validation vectors into strictly typed Pandas DataFrames matching the operational baseline schema.

## 📊 Evaluation Metrics
* **Algorithm**: Random Forest Classifier (Ensemble Method)
* **Metrics Computed**: Precision, Recall, F1-Score, and Support via a comprehensive classification report.
* **Accuracy Target**: ≥ 95% deterministic classification accuracy on the validation partition.

