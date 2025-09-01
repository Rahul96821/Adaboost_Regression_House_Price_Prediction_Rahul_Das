Overview

This project focuses on predicting house prices using the King County Housing Dataset (Seattle, USA). The dataset contains 21 features describing various aspects of houses such as living area, bedrooms, bathrooms, location, and renovation details.

The goal of this project is to apply machine learning regression techniques—specifically AdaBoost Regressor—to understand how different property features influence house prices and to build a predictive model.

Dataset

Total entries: 21,613

Features: 21 (numeric + categorical)

Target variable: price (House Sale Price)

Key features considered for modeling:

sqft_living

grade

sqft_above

sqft_living15

bathrooms

view

sqft_basement

waterfront

yr_built

lat, long

bedrooms

Methods

Data Exploration & Cleaning

Verified missing values (none found).

Selected relevant numeric features.

Explored feature correlation with price.

Feature Selection

Based on correlation analysis, selected the most important features influencing price.

Model Training

Applied AdaBoost Regressor with:

n_estimators = 50

learning_rate = 0.2

loss = 'exponential'

Split dataset into 80% training and 20% testing.

Evaluation Metrics

R² Score

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Results

Training R² Score: 0.696

Testing R² Score: 0.644

MSE: 4.43 × 10¹⁰

RMSE: ≈ 210,394

Key Insights:

Strongest predictors of house prices are: sqft_living, grade, bathrooms, view, and location (lat/long).

Average prediction error is around $210K, which is reasonable given the dataset’s price variability.

Conclusion

The AdaBoost Regressor performed moderately well, explaining about 64% of the variation in house prices on test data. The model highlights that property size, quality (grade), and location are major drivers of housing prices.

However, there is scope for improvement. Future work could include:

Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)

Trying advanced ensemble models like Gradient Boosting, XGBoost, or LightGBM

Feature engineering (e.g., age of house, interaction features)

Outlier detection and removal to reduce RMSE

This project demonstrates the power of ensemble learning in real-estate price prediction and provides valuable insights into housing market dynamics.
