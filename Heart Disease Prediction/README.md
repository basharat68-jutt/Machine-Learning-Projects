# Heart Disease Prediction 🫀

A Machine Learning classification project that predicts whether a person has heart disease based on different medical and clinical features.

## 📌 Project Overview

In this project, a **Gradient Boosting Classifier** is used to predict heart disease.

The project includes:

* Data loading and inspection
* Missing-value checking
* Train/Test Split
* Gradient Boosting Classification
* Model evaluation using Accuracy, Recall, Precision and F1-Score
* Hyperparameter Tuning using `GridSearchCV`
* User input based prediction

## 📊 Dataset

The dataset contains **1,025 records** and **14 columns**.

### Features

| Feature    | Description                           |
| ---------- | ------------------------------------- |
| `age`      | Age of the patient                    |
| `sex`      | Sex of the patient                    |
| `cp`       | Chest pain type                       |
| `trestbps` | Resting blood pressure                |
| `chol`     | Cholesterol level                     |
| `fbs`      | Fasting blood sugar                   |
| `restecg`  | Resting electrocardiographic results  |
| `thalach`  | Maximum heart rate achieved           |
| `exang`    | Exercise-induced angina               |
| `oldpeak`  | ST depression                         |
| `slope`    | Slope of the peak exercise ST segment |
| `ca`       | Number of major vessels               |
| `thal`     | Thalassemia                           |
| `target`   | Heart disease target                  |

The target variable is `target`.

## 🔍 Data Inspection

The dataset was inspected using:

```python
df.info()
df.isnull().sum()
```

There are **no missing values** in the dataset.

## 🤖 Machine Learning Model

The project uses:

```python
GradientBoostingClassifier()
```

The data was divided into training and testing sets using:

```python
train_test_split(
    x,
    y,
    test_size=0.2,
    random_state=42
)
```

## 📈 Initial Model Performance

The initial Gradient Boosting model achieved:

* **Accuracy:** 93.17%
* **Recall:** 95.15%

### Classification Report

| Class | Precision | Recall | F1-Score |
| ----- | --------: | -----: | -------: |
| 0     |      0.95 |   0.91 |     0.93 |
| 1     |      0.92 |   0.95 |     0.93 |

Overall:

* **Accuracy:** 93%
* **Macro F1-Score:** 93%
* **Weighted F1-Score:** 93%

## ⚙️ Hyperparameter Tuning

`GridSearchCV` was used with **5-fold cross-validation** to find better Gradient Boosting parameters.

### Parameter Grid

```python
param_grid = {
    'n_estimators': [100, 200],
    'learning_rate': [0.05, 0.1],
    'max_depth': [2, 3],
    'min_samples_split': [2, 5],
    'min_samples_leaf': [1, 2]
}
```

### Best Parameters

```text
learning_rate = 0.1
max_depth = 3
min_samples_leaf = 1
min_samples_split = 2
n_estimators = 200
```

The best cross-validation accuracy was:

**98.17%**

## 🏆 Final Model Performance

After applying the best hyperparameters, the Gradient Boosting model achieved:

**Accuracy: 98.54%**

```text
Accuracy = 98.54%
```

This shows a significant improvement over the initial model's **93.17% accuracy**.

## 👤 User Input Prediction

The project also allows users to enter patient information manually.

The model takes the following inputs:

```text
Age
Sex
Chest Pain Type
Resting Blood Pressure
Cholesterol
Fasting Blood Sugar
Resting ECG
Maximum Heart Rate
Exercise-Induced Angina
Oldpeak
Slope
Number of Major Vessels
Thalassemia
```

The trained model then predicts whether heart disease is present.

### Prediction Output

If the model predicts `0`:

```text
Congratulations! You Have No Heart Disease.
```

If the model predicts `1`:

```text
You Have Heart Disease!
```

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

## 📚 Machine Learning Concepts Practiced

This project demonstrates practical use of:

* Classification
* Train/Test Split
* Gradient Boosting
* Accuracy Score
* Recall Score
* Precision
* F1-Score
* Classification Report
* Hyperparameter Tuning
* GridSearchCV
* Cross-Validation
* User Input Prediction

## 📁 Project Structure

```text
Heart-Disease-Prediction/
│
├── Heart Disease Prediction.ipynb
├── Heart File.csv
└── README.md
```

## 🚀 Future Improvements

* Add Confusion Matrix visualization
* Add more data visualizations and EDA
* Compare multiple classification algorithms
* Add Precision, Recall and F1-Score after hyperparameter tuning
* Build an interactive Streamlit application
* Deploy the trained model

## ⚠️ Disclaimer

This project is created for **educational and machine learning practice purposes**. The predictions should not be considered a medical diagnosis or a replacement for professional medical advice.
