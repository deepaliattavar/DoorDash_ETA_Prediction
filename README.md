# DoorDash ETA Prediction

This project focuses on predicting estimated delivery times (ETAs) for DoorDash orders using a real-world dataset of over 190,000 orders. By analyzing delivery patterns, cleaning and preprocessing the data, and applying various regression models, we aimed to improve the accuracy and reliability of ETA predictions.

## Dataset

- **Source:** Kaggle (DoorDash Delivery ETA Dataset)
- **Size:** ~190,000 orders
- **Features:** Pickup/delivery timestamps, store/driver/customer info, distances, market IDs, etc.

## Key Techniques

- **Data Cleaning:** Removed duplicates, handled missing timestamps, encoded categorical variables.
- **Feature Engineering:** Extracted time-based features, calculated distances, grouped by zones/markets.
- **Outlier Removal:** Used Z-score to remove extreme delivery durations.
- **Imputation:** Replaced nulls using median/zero strategies based on feature behavior.
- **Scaling:** Applied min-max normalization and standardization to test effects on model accuracy.

## Models Applied

- **Baseline:** Linear Regression, Ridge Regression  
- **Tree-Based Models:** Random Forest, XGBoost Regressor  
- **Evaluation Metrics:** MAE, RMSE, R² Score

- **Best Model:** XGBoost Regressor with preprocessing (R²: 0.4938)
- **Impact:** ETA prediction error reduced by nearly 2× with effective preprocessing and feature selection.

## Key Insights

- Timestamp features and zone/market clustering improved model performance.
- Preprocessing (imputation + scaling) significantly impacted accuracy.
- Feature importance showed driver and store delays as critical variables.
