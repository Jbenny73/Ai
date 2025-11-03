# Vehicle Price Prediction

A machine learning project to predict vehicle prices using regression techniques on data from vehicle listings.

## Overview

This project implements several regression models to predict vehicle prices based on features such as:
- Year, Brand, Model, and Edition
- Condition (New/Used)
- Transmission type (Automatic/Manual)
- Body type
- Fuel type (Petrol, Diesel, Hybrid, Electric)
- Engine capacity and mileage

## Models Implemented

1. **Linear Regression** - Baseline linear model
2. **Ridge Regression** - L2 regularized linear model with hyperparameter tuning
3. **k-Nearest Neighbors (kNN)** - Non-parametric regression model with hyperparameter tuning

## Key Features

- **Data Cleaning**: Automated cleaning of price, mileage, and capacity fields from string format
- **Feature Engineering**: 
  - Car age calculation
  - Brand popularity scoring
  - Fuel type flags (Hybrid, Petrol, Diesel, Electric)
  - Transmission and condition flags
- **Pipeline-based Approach**: Uses sklearn's Pipeline and ColumnTransformer for reproducible preprocessing
- **Model Selection**: Grid Search CV for hyperparameter optimization
- **Evaluation**: Cross-validation to assess model performance and detect overfitting

## Results

- **Best Model**: k-Nearest Neighbors Regressor
- **Test MAE**: ~789,000 LKR

## Installation

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/vehicle-price-prediction.git
cd vehicle-price-prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the notebook:
```bash
jupyter notebook ai1.ipynb
```

## Dataset

The dataset contains 18,938 vehicle listings with 19 features. After cleaning and filtering outliers, 18,038 records were used for training and testing.

## Methodology

1. Load and shuffle the dataset
2. Clean price, mileage, and capacity columns
3. Filter outliers using IQR method
4. Split data into 80% training/dev and 20% testing
5. Apply feature engineering transformations
6. Train and compare multiple regression models
7. Select best model using cross-validation
8. Evaluate on held-out test set

## References

This project is based on coursework material from AI1 lecture series, specifically:
- AI1_11_regression_case_study.ipynb - Pipeline structure and custom transformers
- AI1_08_model_selection.ipynb - GridSearchCV implementation

## License

MIT License

