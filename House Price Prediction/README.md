# 🏠 House Price Prediction

A Machine Learning regression project that predicts house prices based on different property features such as bedrooms, bathrooms, living area, lot size, floors, waterfront, view, condition, and location.

## 📌 Project Overview

In this project, I built a **House Price Prediction model** using Python and Scikit-learn.

The project includes:

* Data loading and exploration
* Missing-value checking
* Date feature extraction
* Categorical feature encoding using One-Hot Encoding
* Train/Test split
* Gradient Boosting Regression
* Model evaluation using MAE, MSE, and R²
* Hyperparameter tuning using GridSearchCV
* Interactive user input for house-price prediction

## 📊 Dataset Features

The dataset contains information about houses, including:

* `bedrooms`
* `bathrooms`
* `sqft_living`
* `sqft_lot`
* `floors`
* `waterfront`
* `view`
* `condition`
* `sqft_above`
* `sqft_basement`
* `yr_built`
* `yr_renovated`
* `date`
* `city`
* `statezip`
* `country`
* `price`

The `date` column was converted into:

* `year`
* `month`

The target variable is:

```text
price
```

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked dataset information and missing values.
3. Converted the `date` column into datetime format.
4. Extracted `year` and `month` from the date.
5. Removed unnecessary columns such as:

   * `date`
   * `street`
   * `country`
   * `price` from the feature dataset
6. Applied **One-Hot Encoding** to categorical columns:

   * `city`
   * `statezip`

## 🤖 Machine Learning Model

The main model used in this project is:

**GradientBoostingRegressor**

Initial model parameters:

```python
GradientBoostingRegressor(
    learning_rate=0.1,
    max_depth=2,
    min_samples_leaf=2,
    min_samples_split=2,
    n_estimators=300
)
```

The dataset was divided into training and testing sets using:

```python
train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=42
)
```

## 📏 Model Evaluation

The model was evaluated using:

### MAE — Mean Absolute Error

Measures the average absolute difference between actual and predicted house prices.

### MSE — Mean Squared Error

Squares the prediction errors before calculating their average, giving more weight to larger errors.

### R² Score

Measures how well the model explains the variation in house prices.

```python
mean_absolute_error(y_test, y_pred)
mean_squared_error(y_test, y_pred)
r2_score(y_test, y_pred)
```

## 🔧 Hyperparameter Tuning

`GridSearchCV` was used to search for better Gradient Boosting parameters.

Parameters tested included:

```python
n_estimators
learning_rate
max_depth
min_samples_split
min_samples_leaf
```

The search used:

```python
cv=5
scoring='r2'
n_jobs=-1
```

The best parameters were then used to train the final Gradient Boosting model.

## 🏡 Interactive Prediction

The project also allows the user to enter house information manually, including:

```text
Bedrooms
Bathrooms
Living Area
Lot Size
Floors
Waterfront
View
Condition
Above Ground Area
Basement Area
Year Built
Renovation Year
Selling Year
Selling Month
City
State ZIP
```

The trained model then predicts the estimated house price.

Example:

```text
Predicted Price is: 307,000.00
```

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 📂 Project Structure

```text
House-Price-Prediction/
│
├── House Price Prediction.ipynb
├── House Prediction.csv
└── README.md
```

## 🎯 Learning Outcomes

Through this project, I practiced:

* Regression problems
* Feature preprocessing
* One-Hot Encoding
* Train/Test splitting
* Gradient Boosting
* Model evaluation
* Hyperparameter tuning
* GridSearchCV
* Interactive model prediction
* Building a complete Machine Learning workflow

## 🚀 Future Improvements

Possible improvements for this project include:

* Better feature engineering
* Trying additional regression algorithms
* Using a complete Scikit-learn Pipeline
* Comparing multiple models
* Improving prediction of high-priced houses
* Further hyperparameter optimization
* Deploying the model as a web application

---

**Project Type:** Machine Learning — Regression
**Model:** Gradient Boosting Regressor
**Target:** House Price
