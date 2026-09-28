# 🏠 House Price Prediction using Scikit-learn Pipeline

A Machine Learning regression project that predicts house prices using a **Scikit-learn Pipeline** and **Gradient Boosting Regressor**.

The project demonstrates how data preprocessing and model training can be combined into a single pipeline, making the workflow cleaner and easier to use for new predictions.

## 📌 Project Overview

In this project, I built a house price prediction model using:

* Pandas
* NumPy
* Scikit-learn
* One-Hot Encoding
* ColumnTransformer
* Pipeline
* GradientBoostingRegressor

The model predicts house prices based on property characteristics and location information.

## 📊 Dataset Features

The dataset contains house-related features such as:

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

The target variable is:

```text
price
```

## 🔧 Data Preprocessing

The `date` column was converted into a datetime format and two new features were extracted:

* `year`
* `month`

The following columns were removed:

```text
street
country
date
```

Categorical features were encoded using **OneHotEncoder**:

```python
OneHotEncoder(
    sparse_output=False,
    handle_unknown='ignore'
)
```

The categorical columns used for encoding were:

```text
city
statezip
```

## 🔄 Scikit-learn Pipeline

A Scikit-learn `Pipeline` was used to combine preprocessing and model training.

The pipeline contains:

```python
pipe = Pipeline([
    ('trf1', trf1),
    ('trf3', trf3)
])
```

### ColumnTransformer

`ColumnTransformer` was used to apply One-Hot Encoding to the categorical columns while keeping the remaining numerical columns unchanged.

```python
trf1 = ColumnTransformer([
    (
        'ohe',
        OneHotEncoder(
            sparse_output=False,
            handle_unknown='ignore'
        ),
        ['city', 'statezip']
    )
], remainder='passthrough')
```

Using `handle_unknown='ignore'` allows the pipeline to handle previously unseen categorical values during prediction.

## 🤖 Machine Learning Model

The regression model used in this project is:

**GradientBoostingRegressor**

The model parameters are:

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
    test_size=0.2,
    random_state=42
)
```

## 📏 Model Evaluation

The model was evaluated using:

### R² Score

Measures how well the model explains the variation in house prices.

```python
r2_score(y_test, y_pred)
```

### MAE — Mean Absolute Error

Measures the average absolute difference between the actual and predicted house prices.

```python
mean_absolute_error(y_test, y_pred)
```

## 🏡 Interactive House Price Prediction

After training, the project allows the user to enter information about a new house.

The user provides:

```text
Bedrooms
Bathrooms
Sqft Living
Sqft Lot
Floors
Waterfront
View
Condition
Sqft Above
Sqft Basement
Year Built
Year Renovated
Selling Year
Selling Month
City
StateZip
```

The entered information is converted into a DataFrame and passed directly to the trained pipeline:

```python
predicted_price = pipe.predict(new_data)
```

The pipeline automatically performs the required preprocessing before generating the prediction.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

## 📂 Project Structure

```text
Pipeline-House-Price-Prediction/
│
├── Pipeline-House Price Price Prediction.ipynb
├── House Prediction.csv
└── README.md
```

## 🎯 Learning Outcomes

Through this project, I practiced:

* Regression
* Data preprocessing
* Feature engineering
* One-Hot Encoding
* ColumnTransformer
* Scikit-learn Pipeline
* Gradient Boosting Regression
* Train/Test Split
* Model evaluation
* Handling unknown categorical values
* Making predictions on new user input

## 🚀 Future Improvements

Possible improvements for this project include:

* Adding feature scaling where appropriate
* Comparing different regression algorithms
* Performing additional hyperparameter tuning
* Improving prediction accuracy for high-priced houses
* Adding cross-validation
* Deploying the model as a web application

---

**Project Type:** Machine Learning — Regression
**Model:** Gradient Boosting Regressor
**Preprocessing:** One-Hot Encoding + ColumnTransformer
**Workflow:** Scikit-learn Pipeline
**Target:** House Price
