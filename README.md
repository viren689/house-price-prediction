# 🏠 House Price Prediction Using Machine Learning

##  Project Overview

This project focuses on predicting house prices using machine learning
regression algorithms.

The objective is to build, evaluate, compare, and interpret multiple
machine learning models using property characteristics such as area,
bedrooms, bathrooms, age, location, and property type.

The project demonstrates a complete machine learning workflow from data
exploration and preprocessing to model training, evaluation, visualization,
and final model selection.

---

##  Objectives

- Understand the fundamentals of machine learning regression.
- Explore and understand the house price dataset.
- Handle numerical and categorical features.
- Perform train-test splitting.
- Implement Linear Regression from scratch.
- Build machine learning models using Scikit-Learn.
- Evaluate models using MAE, MSE, RMSE, and R².
- Compare multiple regression algorithms.
- Identify important features.
- Visualize actual versus predicted house prices.
- Select the best-performing model.

---

##  Dataset

The dataset contains **300 house/property records**.

### Features

| Feature | Description |
|---|---|
| Property_ID | Unique property identifier |
| Area | Property area |
| Bedrooms | Number of bedrooms |
| Bathrooms | Number of bathrooms |
| Age | Property age |
| Location | Property location |
| Property_Type | Type of property |
| Price | House price / target variable |

The target variable is:  Price

Property_ID was excluded from model training because it is an identifier
rather than a predictive feature.

##  Technologies Used
Python
Pandas
NumPy
Matplotlib
Scikit-Learn
Jupyter Notebook
Git
GitHub

##  Machine Learning Models

The following models were evaluated:

Linear Regression From Scratch
Scikit-Learn Linear Regression
Polynomial Regression
Decision Tree Regression
Random Forest Regression

##  Evaluation Metrics

The models were evaluated using:

MAE

Mean Absolute Error measures the average absolute difference between actual
and predicted values.

Lower values indicate better performance.

MSE

Mean Squared Error measures the average squared prediction error.

Lower values indicate better performance.

RMSE

Root Mean Squared Error is the square root of MSE and is expressed in the
same units as the target variable.

Lower values indicate better performance.

R² Score

R² measures how much of the variation in house prices is explained by the
model.

Higher values indicate better performance.

##  Model Performance
Model	MAE	MSE	RMSE	R²
Linear Regression	₹2,188,736	₹8.45 × 10¹²	₹2,907,633	0.940637
Polynomial Regression	₹714,541	₹8.03 × 10¹¹	₹896,288	0.994359
Decision Tree	₹2,414,778	₹9.84 × 10¹²	₹3,136,179	0.930938
Random Forest	₹1,479,208	₹3.90 × 10¹²	₹1,974,060	0.972637

##  Best Model

Polynomial Regression

R² Score:

0.994359

The model achieved approximately 99.44% R² on the test dataset.

It also achieved the lowest MAE, MSE, and RMSE among the evaluated models.

##  Feature Importance

Feature importance was analyzed using the Random Forest model.

The most important features were:

Feature	Importance
Area	0.685596
Location - City Center	0.151541
Location - Rural	0.099433
Location - Suburb	0.031825
Bedrooms	0.019685
Age	0.007945
Bathrooms	0.001759
Key Finding

Area was the most influential feature in the Random Forest model,
followed by location-related features.

Feature importance represents the model's relative reliance on a feature and
should not be interpreted as a direct percentage change in house price.

##  Visualization

The project includes an Actual vs Predicted visualization for the final
Polynomial Regression model.

The visualization shows that most predicted values are close to the actual
house prices and the perfect-prediction reference line.

The visualization supports the strong performance indicated by the
evaluation metrics.

##  Project Structure
Week9-House-Price-Prediction/
│
├── house_price_prediction.ipynb
├── house_prices.csv
├── model_evaluation_report.md
├── requirements.txt
├── predictions_vs_actual.png
└── README.md


## Installation
1. Clone the repository
git clone <YOUR_GITHUB_REPOSITORY_URL>
2. Navigate to the project directory
cd Week9-House-Price-Prediction
3. Create a virtual environment
python -m venv .venv
4. Activate the virtual environment

Windows PowerShell:

.venv\Scripts\Activate.ps1
5. Install dependencies
pip install -r requirements.txt
6. Start Jupyter Notebook
jupyter notebook

Open:

house_price_prediction.ipynb

and run the notebook cells.

## Testing and Validation

The project uses a train-test split to evaluate model performance on data
that was not used during model training.

The same test dataset was used to compare all regression models.

The following metrics were calculated:

MAE
MSE
RMSE
R²

This provides multiple perspectives for evaluating prediction performance.

##  Key Insights
House price has a strong relationship with property area.
Location is another important factor affecting predictions.
Linear Regression provided a strong baseline.
The residual analysis suggested possible non-linear relationships.
Polynomial Regression achieved the best performance on the test dataset.
Random Forest performed better than Linear Regression and Decision Tree.
The final Polynomial Regression model achieved an R² score of 0.994359.

##  Limitations
The dataset contains only 300 records.
Results are based on a single train-test split.
The dataset may not represent all real-world housing markets.
Polynomial Regression performance may vary with different datasets.
Additional validation using unseen data would be required before real-world
deployment.


## Future Improvements

Possible improvements include:

Hyperparameter tuning.
Cross-validation.
Testing additional regression algorithms.
Using larger real-world housing datasets.
Feature engineering.
Outlier detection and treatment.
Model deployment through a web application.
Creating an interactive house price prediction interface.


## Author

Viren Wankhade

GitHub: https://github.com/viren689

LinkedIn: https://www.linkedin.com/in/viren-wankhade