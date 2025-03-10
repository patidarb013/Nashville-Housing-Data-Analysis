# Nashville-Housing-Data-Analysis

# Project Overview
This project focuses on analyzing Nashville housing market data using predictive analytics techniques. The dataset contains various property attributes, and the analysis aims to clean, preprocess, and build machine learning models to predict whether a property's sale price is "Over" or "Under" its value.

# Dataset Information
Dataset Used: Nashville_housing_data.csv

# Key Features:
- **Year Built**: Construction year of the property
- **Finished Area**: Total livable area in square feet
- **Full Bath, Half Bath**: Number of bathrooms
- **Foundation Type**: Type of foundation (used to determine basement presence)
- **Sale Price Compared To Value**: Binary target variable (Over or Under)

# Data Cleaning & Preprocessing
## Handling Missing Values:
- **Used SimpleImputer to fill missing values**.
- **Dropped unnecessary columns (Unnamed: 0, Suite/Condo #, Property City)**.
- **Removed rows with missing values (dropna())**.
- **Eliminated duplicate records (drop_duplicates())**.

## Feature Engineering:
- **Property Age: Current Year - Year Built**
- **Total Bathrooms: Full Bath + (0.5 * Half Bath)**
- **Basement Indicator: 1 if 'BSMT' in Foundation Type else 0**

# Machine Learning Models Implemented
## 1. Logistic Regression
- **Goal: Predict whether a house is "Over" or "Under" its value**.
- **Features Used: Property age, total bathrooms, basement presence**.
- **Performance Evaluation: Used classification report (Precision, Recall, F1-score)**.

## 2. Decision Tree Classifier
- **Goal: Classify housing prices using a tree-based approach**.
- **Features Used: Property age, total bathrooms, basement presence**.
- **Advantage: Captures non-linear relationships in the data**.

## 3. Gradient Boosting Classifier
- **Goal: Improve predictive accuracy using ensemble learning**.
- **Features Used: Finished area, year built**.
- **Advantage: Reduces overfitting, performs well on structured data**.

## 4. Model Comparison
- **Evaluated four models**:
Logistic Regression
Decision Tree
Random Forest Classifier
Gradient Boosting Classifier
Compared classification reports for accuracy, precision, recall, and F1-score.

# Results & Insights
- **Data cleaning improved model accuracy by ensuring consistency**.
- **Gradient Boosting outperformed other models, showing high precision and recall**.
- **Feature Engineering added valuable predictors, such as property age and basement presence**.
- **Decision Trees provided interpretable results, but were prone to overfitting**.

# Tools & Libraries Used
## Programming Language: Python
## Libraries:
- **pandas – Data manipulation**
- **numpy – Numerical computations**
- **sklearn – Machine learning models**
- **matplotlib, seaborn – Data visualization**

# Conclusion & Future Work
The Gradient Boosting model performed best, making it the ideal choice for predicting property sale prices.

# Future improvements:
- **Incorporate more real estate features (e.g., neighborhood details)**.
- **Use deep learning models for enhanced accuracy**.
- **Perform hyperparameter tuning to further optimize models**.

# References
- **https://towardsdatascience.com/how-to-clean-your-data-in-python-8f178638b98d**
- **https://www.datacamp.com/tutorial/understanding-logistic-regression-python**
- **https://scikit-learn.org/stable/modules/tree.html**
- **https://www.datacamp.com/tutorial/guide-to-the-gradient-boosting-algorithm**
