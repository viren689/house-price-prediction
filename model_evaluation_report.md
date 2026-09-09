# Model Evaluation Report

## 1. Project Overview

This project focuses on predicting house prices using machine learning
regression techniques.

The dataset contains 300 property records with features including:

- Area
- Bedrooms
- Bathrooms
- Age
- Location
- Property Type
- Price

The objective was to develop and evaluate multiple regression models and
identify the best-performing approach for house price prediction.

---

## 2. Data Preparation

The dataset was inspected for missing values, data types, and available
features.

No missing values were found in the dataset.

`Property_ID` was excluded from model training because it is an identifier
rather than a predictive feature.

Numerical features included:

- Area
- Bedrooms
- Bathrooms
- Age

Categorical features included:

- Location
- Property Type

Categorical variables were converted into numerical representations using
One-Hot Encoding.

The dataset was divided into training and testing sets using a train-test
split with a fixed random state to ensure reproducibility.

---

## 3. Models Evaluated

The following regression models were evaluated:

1. Linear Regression from Scratch
2. Scikit-Learn Linear Regression
3. Polynomial Regression
4. Decision Tree Regression
5. Random Forest Regression

---

## 4. Evaluation Metrics

The models were evaluated using four regression metrics.

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted
values.

Lower MAE indicates better performance.

### Mean Squared Error (MSE)

MSE calculates the average squared prediction error and gives greater weight
to larger errors.

Lower MSE indicates better performance.

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and is expressed in the same units as the
target variable.

Lower RMSE indicates better performance.

### R² Score

R² measures the proportion of variation in the target variable explained by
the model.

Higher R² indicates better performance.

---

## 5. Model Performance

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Linear Regression | ₹2,188,736 | ₹8.45 × 10¹² | ₹2,907,633 | 0.940637 |
| Polynomial Regression | ₹714,541 | ₹8.03 × 10¹¹ | ₹896,288 | 0.994359 |
| Decision Tree | ₹2,414,778 | ₹9.84 × 10¹² | ₹3,136,179 | 0.930938 |
| Random Forest | ₹1,479,208 | ₹3.90 × 10¹² | ₹1,974,060 | 0.972637 |

---

## 6. Best Performing Model

Polynomial Regression achieved the best overall performance on the test
dataset.

### Performance

- MAE: approximately ₹714,541
- MSE: approximately ₹8.03 × 10¹¹
- RMSE: approximately ₹896,288
- R²: 0.994359

The model achieved an R² score of approximately 99.44%, indicating that it
explains a very large proportion of the variation in house prices in this
test dataset.

Polynomial Regression also achieved the lowest MAE, MSE, and RMSE among the
models evaluated.

---

## 7. Feature Importance

Feature importance was analyzed using the Random Forest model.

The most important features were:

| Feature | Importance |
|---|---:|
| Area | 0.685596 |
| Location - City Center | 0.151541 |
| Location - Rural | 0.099433 |
| Location - Suburb | 0.031825 |
| Bedrooms | 0.019685 |
| Age | 0.007945 |
| Bathrooms | 0.001759 |

Area was the most influential feature in the Random Forest model, followed
by location-related features.

Feature importance represents the model's relative reliance on each feature.
It should not be interpreted as a direct percentage change in house price.

---

## 8. Prediction Visualization

The `predictions_vs_actual.png` visualization compares the actual house
prices with the prices predicted by the final Polynomial Regression model.

Most observations are positioned close to the perfect-prediction reference
line, which indicates that the model's predictions are generally close to
the actual values.

The visualization supports the strong evaluation results obtained from the
Polynomial Regression model.

---

## 9. Key Insights

1. Property area was the most important feature identified by the Random
   Forest model.

2. Location also had a substantial influence on model predictions.

3. Scikit-Learn Linear Regression provided a strong baseline with an R²
   score of 0.940637.

4. Polynomial Regression significantly improved the prediction performance
   and achieved the highest R² score of 0.994359.

5. Random Forest performed better than both Linear Regression and Decision
   Tree Regression on this test dataset.

6. The residual analysis from Linear Regression showed evidence of
   non-linear relationships, providing motivation for testing Polynomial
   Regression.

---

## 10. Limitations

The results are based on the available dataset and a single train-test split.

The dataset contains only 300 property records, so the results may not
generalize to all real-world housing markets.

Polynomial Regression can also become sensitive to the training data when
higher-degree features are introduced.

The model should therefore be validated using additional unseen data before
being considered for real-world deployment.

---

## 11. Conclusion

This project demonstrated a complete machine learning workflow for house
price prediction, including data exploration, preprocessing, train-test
splitting, model development, evaluation, visualization, comparison, and
interpretation.

Among the tested models, Polynomial Regression achieved the best performance
on the test dataset, with an R² score of 0.994359.

The project demonstrates how machine learning can be used to identify
relationships between property characteristics and house prices while also
highlighting the importance of evaluating multiple models before selecting
a final approach.
