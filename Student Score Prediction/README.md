# Student Score Prediction using Linear Regression

This project uses **Linear Regression** to predict a student's final exam score based on their **study hours per week**.

## 📌 Project Overview

The model learns the relationship between:

* **Input:** Study Hours per Week
* **Output:** Final Exam Score

After training, the model can predict the expected final score for a given number of study hours.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

## 📊 Dataset

The project uses a dataset containing student information with the following important columns:

* `Study_Hours_per_Week`
* `Final_Score`

## 🤖 Machine Learning Model

The project uses:

**Linear Regression**

The model is trained using `Study_Hours_per_Week` as the input feature and `Final_Score` as the target variable.

## 📈 Model Evaluation

The following regression metrics are used to evaluate the model:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

## 📉 Visualizations

The project includes:

1. Distribution of students' final exam scores using a histogram.
2. Scatter plot showing actual scores.
3. Regression line showing the relationship between study hours and final scores.

## 🔮 Prediction

After training the model, it can be used to predict a student's final score.

For example, the project predicts the expected final score for a student who studies **9 hours per week**.

## 🎯 Learning Objectives

This project helped practice:

* Loading datasets with Pandas
* Separating features and target variables
* Training a Linear Regression model
* Making predictions
* Evaluating regression models
* Visualizing data and regression results
* Making predictions for new input values

## 📁 Project Structure

```text
Student-Score-Prediction/
│
├── student_score_prediction.py
├── student_dataset_5000.csv
└── README.md
```

## 🚀 Future Improvements

* Use multiple features such as attendance, previous scores, and assignments.
* Split the dataset into training and testing sets.
* Compare Linear Regression with other regression algorithms.
* Perform feature engineering and hyperparameter tuning.
