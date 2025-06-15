# UPDRS Motor Score Prediction: Multi-Modal Modeling

**Objective**: Predict Unified Parkinson's Disease Rating Scale (UPDRS) motor scores using multi-modal data including:
- Structural MRI measurements
- DAT-SPECT imaging
- APOE4 genotype
- Demographic information (Age, Sex)

## Experiment Progression

### 1. Baseline Model Exploration
- **Approach**: 
  - Compared Linear Regression vs. Random Forest Regressor
  - Used preprocessed dataset with imputed values
- **Key Findings**:
  - Linear Regression showed poor predictive performance
  - Random Forest demonstrated significantly better results
- **Performance**:MAE: ~6.8, R²: ~0.45 (Initial implementation)



### 2. Advanced Model Comparison & Feature Engineering
- **Approach**:
- Tested LightGBM and XGBoost with hyperparameter tuning
- Applied Recursive Feature Elimination (RFE) to select top 25 features
- **Key Findings**:
- Feature selection improved all models
- Random Forest remained superior to gradient boosting methods
- **Performance Comparison**:
| Model       | MAE   | MSE   | R²    |
|-------------|-------|-------|-------|
| LightGBM    | 6.539 | 74.711| 0.495 |
| XGBoost     | 6.525 | 76.952| 0.480 |
| Random Forest| 5.681 | 56.947| 0.579 |

### 3. Advanced Feature Engineering & Model Optimization
- **Approach**:
- Created novel interaction features:
  - Striatal-Entorhinal Network Interaction
  - Asymmetry-Weighted Striatal Score
  - White Matter Integrity Index
  - Age-Adjusted Striatal Binding
  - Ventricular Effect Score
- Conducted Randomized Search for Random Forest hyperparameters
- Tested shallow ANN with early stopping
- **Key Findings**:
- Feature engineering further improved model performance
- Random Forest outperformed ANN approach
- Best performance approaching clinical utility thresholds
- **Performance**:Optimized Random Forest:
          MAE: 5.720, MSE: 55.963, RMSE: 7.481, R²: 0.586

          Shallow ANN:
          MAE: 6.985, R²: 0.411

  ## Next Steps
1. Incorporate additional clinical features
2. Try further Tunning or feature engineering 
