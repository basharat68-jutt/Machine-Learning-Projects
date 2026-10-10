# 🚢 Titanic Survival Prediction

## 📌 Project Overview
This project uses Machine Learning to predict whether a passenger would survive the Titanic disaster. A **Random Forest Classifier** is trained using passenger information and evaluated using classification metrics.

The project also allows users to enter passenger details and get a survival prediction.

## 🎯 Objectives
- Analyze the Titanic dataset.
- Handle missing values using `SimpleImputer`.
- Convert categorical features into numerical values using `OneHotEncoder`.
- Train a `RandomForestClassifier`.
- Evaluate the model using Accuracy, Precision, and Recall.
- Predict survival based on user-provided passenger details.

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## 📂 Dataset
The project uses the Titanic dataset, which contains passenger information such as:

- `Pclass` — Passenger class
- `Sex` — Passenger's sex
- `Age` — Passenger's age
- `SibSp` — Number of siblings or spouses aboard
- `Parch` — Number of parents or children aboard
- `Embarked` — Port of embarkation
- `Survived` — Target variable (0 = Did not survive, 1 = Survived)

## ⚙️ Project Workflow
1. **Data Exploration:** Inspect the dataset, data types, descriptive statistics, and missing values.
2. **Data Preprocessing:** Fill missing age values and replace missing embarkation values with the most frequent category.
3. **Encoding:** Apply One-Hot Encoding to the `Sex` and `Embarked` columns.
4. **Feature Selection:** Remove selected columns that are not used in the model.
5. **Train-Test Split:** Split the data into 80% training and 20% testing sets.
6. **Model Training:** Train a Random Forest Classifier.
7. **Model Evaluation:** Calculate Accuracy, Precision, and Recall.
8. **Custom Prediction:** Accept passenger details as input and predict survival.

## 📊 Evaluation Metrics
- **Accuracy:** Measures the proportion of correct predictions.
- **Precision:** Measures how many passengers predicted to survive actually survived.
- **Recall:** Measures how many passengers who actually survived were correctly identified.

## ▶️ How to Run
1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install pandas numpy scikit-learn jupyter
   ```

3. Place the Titanic dataset in the appropriate location and update the CSV file path in the notebook.
4. Open `Titanic Survival Prediction.ipynb` in Jupyter Notebook or VS Code.
5. Run the notebook cells in order.
6. Enter passenger details when prompted to get a survival prediction.

## 📁 Project Structure

```text
Titanic-Survival-Prediction/
├── Titanic Survival Prediction.ipynb
├── Titanic-Dataset.csv
└── README.md
```

## 🚀 Future Improvements
- Use a Scikit-learn Pipeline for preprocessing and model training.
- Compare Random Forest with Logistic Regression and other classifiers.
- Perform hyperparameter tuning using GridSearchCV.
- Add a confusion matrix and F1-score for more comprehensive evaluation.
- Build an interactive web application using Streamlit.

## 👨‍💻 Author
**Machine Learning Portfolio Project**

