# 🚢 Titanic Survival Prediction - Logistic Regression


## 🧠 Skills Applied

- Logistic Regression
- Data Cleaning and Preprocessing
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Model Evaluation (Accuracy, Confusion Matrix)
- Interpretation of Coefficients

---

## 🗂 Dataset

The dataset is sourced from [Kaggle's Titanic competition](https://www.kaggle.com/c/titanic/data) and contains the following features:

- **PassengerId**
- **Survived** (Target)
- **Pclass**
- **Name**
- **Sex**
- **Age**
- **SibSp**
- **Parch**
- **Ticket**
- **Fare**
- **Cabin**
- **Embarked**

---

## 🔧 Preprocessing Steps

- Dropped irrelevant columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Handled missing values:
  - Filled `Age` and `Fare` with median
  - Filled `Embarked` with mode
- Categorical Encoding:
  - `Sex`: male → 0, female → 1
  - `Embarked`: S → 0, C → 1, Q → 2
- Feature Scaling using `StandardScaler`

---

## 🚀 Features Used

- `Pclass`
- `Sex`
- `Age`
- `Fare`
- `Embarked`

---

## 📊 Model Used

**Logistic Regression** (from `scikit-learn`)

```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train_scaled, y_train)
