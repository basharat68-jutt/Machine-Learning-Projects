# 🎓 Student Graduation Prediction

## 📌 Project Overview

The **Student Graduation Prediction** project is a Machine Learning classification project that uses student-related data to predict the target class using a Random Forest Classifier.

The project focuses on data preprocessing, feature scaling, training a machine learning model, and evaluating its performance using different classification metrics.

## 🎯 Objectives

* Analyze student data using Pandas and NumPy.
* Encode the target variable using `LabelEncoder`.
* Explore relationships between numerical features using a correlation heatmap.
* Apply feature scaling using `StandardScaler`.
* Split the dataset into training and testing sets.
* Train a `RandomForestClassifier` model.
* Evaluate the model using classification metrics.

## 🛠️ Technologies & Libraries

* **Python** — Programming language
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computing
* **Matplotlib** — Data visualization
* **Seaborn** — Correlation heatmap visualization
* **Scikit-learn** — Data preprocessing, model training, and evaluation

## 📂 Dataset

The project uses a CSV dataset named `student_graduation.csv`.

The dataset contains student-related features, including attendance, scholarship status, gender, tuition fee status, and other educational attributes.

The `Target` column is used as the variable to predict.

**Note:** The CSV dataset must be available locally and its file path must be updated according to your system.

## ⚙️ Project Workflow

### 1. Import Libraries and Load Data

Import the required Python libraries and load the dataset using Pandas.

### 2. Data Exploration

Inspect the dataset and explore its structure, columns, and statistical information. A correlation heatmap is also used to visualize relationships between numerical features.

### 3. Target Encoding

Use `LabelEncoder` to convert the categorical values in the `Target` column into numerical labels.

### 4. Feature Scaling

Apply `StandardScaler` to selected numerical features to standardize their values.

Some binary or categorical columns are excluded from scaling.

### 5. Train-Test Split

Split the data into training and testing sets using `train_test_split`.

* Training data: 80%
* Testing data: 20%
* Random state: 42

### 6. Model Training

Train a `RandomForestClassifier` using the training data.

### 7. Model Evaluation

Evaluate the model's predictions using:

* **Accuracy Score:** Measures the overall proportion of correct predictions.
* **Recall Score:** Measures how effectively the model identifies actual instances of each class, using weighted averaging.
* **F1 Score:** Combines precision and recall into a single metric, using weighted averaging.
* **Confusion Matrix:** Shows the actual versus predicted class counts.

## 🚀 Installation and Usage

### Prerequisites

Make sure Python is installed on your system.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Steps to Run

1. Clone or download this repository.
2. Place `student_graduation.csv` in the appropriate location.
3. Update the CSV file path in the notebook.
4. Open the notebook in Jupyter Notebook or VS Code.
5. Run the notebook cells in order.
6. Review the model evaluation results.

## 📊 Results

The notebook calculates the following evaluation metrics:

* Accuracy Score
* Weighted Recall Score
* Weighted F1 Score
* Confusion Matrix

The actual performance values should be added here after running the notebook.

## 📚 Key Learnings

Through this project, I practiced:

* Data loading and exploration with Pandas.
* Numerical operations with NumPy.
* Target encoding with `LabelEncoder`.
* Feature standardization with `StandardScaler`.
* Training and testing data splitting.
* Classification using Random Forest.
* Model evaluation with Scikit-learn metrics.
* Visualizing correlations using Seaborn.

## 👨‍💻 Author

Created as a Machine Learning practice project to develop practical skills in data preprocessing, classification, and model evaluation.
