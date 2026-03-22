# Bank Churn Modelling

## Overview
This project builds and evaluates machine learning models to predict customer churn in a banking context. It uses XGBoost and Decision Tree classifiers with various data preprocessing and resampling techniques to improve prediction accuracy.

## Project Structure

- **Churn Modelling.ipynb** - Main Jupyter notebook containing all analysis, model training, and evaluation
- **Churn_Modelling.csv** - Raw customer data with features and churn labels
- **best_model.pkl** - Trained XGBoost model saved for future predictions
- **scaler.pkl** - MinMaxScaler fitted on training data for feature normalization
- **Bank_Churn_Data.xlsx** - Original data with model predictions and prediction probabilities
- **Feature_Importance.xlsx** - Feature importance scores from the trained model
- **xgboost_tree.png** - Visualization of the first XGBoost tree

## Key Features

- **Data Cleaning & Exploration** - Comprehensive EDA including null value checks, data distribution analysis, and visualization
- **Feature Engineering** - One-hot encoding of categorical variables and MinMax scaling of numerical features
- **Model Training** - XGBoost classifier with hyperparameter tuning using RandomizedSearchCV
- **Class Imbalance Handling** - SMOTE (Synthetic Minority Oversampling Technique) applied to oversample minority class
- **Model Evaluation** - Confusion matrices, accuracy scores, and feature importance analysis

## Requirements

The following Python libraries are required:
- pandas
- numpy
- scikit-learn
- xgboost
- imbalanced-learn (for SMOTE)
- matplotlib
- seaborn
- plotly
- graphviz
- pillow
- streamlit

## Usage

1. Ensure all dependencies are installed
2. Place `Churn_Modelling.csv` in the project directory
3. Run the Jupyter notebook `Churn Modelling.ipynb` cell by cell
4. Model predictions and outputs will be saved to Excel files

## Model Performance

- Initial XGBoost accuracy improved with SMOTE resampling
- Hyperparameter tuning was performed using RandomizedSearchCV with F1 scoring
- Alternative evaluation metrics (AUC) were tested to improve minority class prediction

## Future Improvements

- Eliminate more outliers for better preprocessing
- Train separate models by geography
- Test additional ensemble methods
- Further optimize for minority class recall

## Output Files

After running the notebook, the following files are generated:
- **Bank_Churn_Data.xlsx** - Predictions and probabilities for all customers
- **Feature_Importance.xlsx** - Model's feature importance rankings
- **best_model.pkl** - Serialized best model for deployment
- **scaler.pkl** - Serialized scaler for data preprocessing
