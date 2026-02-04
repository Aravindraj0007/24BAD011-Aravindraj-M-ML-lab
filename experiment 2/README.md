# ML Lab Experiment 2: Regression and Optimization

This repository contains implementations of Linear and Logistic Regression models with optimization techniques for two different scenarios.

## Table of Contents
- [Overview](#overview)
- [Scenario 1: Linear Regression](#scenario-1-linear-regression)
- [Scenario 2: Logistic Regression](#scenario-2-logistic-regression)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)

## Overview

This experiment demonstrates:
- **Linear Regression** for predicting continuous values (water temperature)
- **Logistic Regression** for binary classification (stock price movement)
- **Regularization techniques** (Ridge and Lasso)
- **Hyperparameter tuning** using GridSearchCV
- **Model evaluation** using various metrics and visualizations

## Scenario 1: Linear Regression

### Objective
Predict water temperature (`T_degC`) based on oceanographic measurements.

### Dataset
- **Files**: `bottle.csv`, `cast.csv`
- **Features**:
  - `Depthm` - Water depth in meters
  - `Salnty` - Salinity level
  - `O2ml_L` - Oxygen concentration
  - `Latitude` - Geographic latitude
  - `Longitude` - Geographic longitude
- **Target**: `T_degC` (Water temperature in degrees Celsius)

### Methodology
1. **Data Preprocessing**:
   - Merged bottle and cast datasets
   - Handled missing values using mean imputation
   - Feature selection and standardization

2. **Models Implemented**:
   - Linear Regression (baseline)
   - Ridge Regression (L2 regularization, α=1)
   - Lasso Regression (L1 regularization, α=0.1)

3. **Evaluation Metrics**:
   - Mean Squared Error (MSE)
   - Root Mean Squared Error (RMSE)
   - R² Score

4. **Visualizations**:
   - Actual vs Predicted scatter plot
   - Residual plot
   - Correlation heatmap

## Scenario 2: Logistic Regression

### Objective
Predict stock price movement direction (up or down) for LICI (Life Insurance Corporation of India).

### Dataset
- **File**: `LICI - minute ata.csv`
- **Features**:
  - `open` - Opening price
  - `high` - Highest price
  - `low` - Lowest price
  - `volume` - Trading volume
- **Target**: `Price_Movement` (1 = price increased, 0 = price decreased)

### Methodology
1. **Data Preprocessing**:
   - Created binary target variable based on close vs open price
   - Handled missing values
   - Feature scaling using StandardScaler

2. **Model Training**:
   - Logistic Regression with default parameters
   - Hyperparameter tuning using GridSearchCV
   - Parameters tested: C=[0.01, 0.1, 1, 10], penalty=['l2'], solver=['lbfgs']

3. **Evaluation Metrics**:
   - Accuracy
   - Precision
   - Recall
   - F1 Score
   - ROC-AUC Score

4. **Visualizations**:
   - Confusion Matrix
   - ROC Curve
   - Feature Importance (Coefficient values)

## Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
```

## Installation

1. Clone or download this repository
2. Install required packages:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

3. Ensure the following data files are in the same directory:
   - `bottle.csv`
   - `cast.csv`
   - `LICI - minute ata.csv`

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook 24BAD011_ML_Lab_exp2.ipynb
```

2. Run all cells sequentially to:
   - Load and preprocess data
   - Train models
   - Generate predictions
   - Visualize results

## Results

### Scenario 1: Linear Regression
- The model successfully predicts water temperature based on oceanographic features
- Evaluation includes MSE, RMSE, and R² scores
- Residual analysis helps identify model performance patterns
- Ridge and Lasso regularization variants are compared

### Scenario 2: Logistic Regression
- Binary classification of stock price movement direction
- High-frequency minute data enables short-term prediction
- Model performance evaluated using multiple classification metrics
- Feature importance reveals which factors most influence price movement
- Hyperparameter tuning improves model accuracy

## File Structure

```
.
├── 24BAD011_ML_Lab_exp2.ipynb    # Main notebook with all code
├── bottle.csv                     # Oceanographic bottle data
├── cast.csv                       # Oceanographic cast data
├── LICI - minute ata.csv         # Stock market minute data
└── README.md                      # This file
```

## Notes

- Data is split 80-20 for training and testing
- Random state is set to 42 for reproducibility
- All features are standardized before model training
- Missing values are handled using mean imputation

## Author

Student ID: 24BAD011

## License

This project is for educational purposes as part of ML Lab coursework.
