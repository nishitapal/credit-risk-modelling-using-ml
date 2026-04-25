# Credit Risk Modeling using Machine Learning

## Project Overview
This project focuses on predicting the credit risk level of loan applicants using Machine Learning. Based on customer financial and behavioral data, the model classifies applicants into different risk categories:

- **P1** = Lowest Risk  
- **P2** = Moderate Risk  
- **P3** = High Risk  
- **P4** = Highest Risk  

This helps banks and financial institutions make better loan approval decisions.

---

## Business Problem Statement
Banks receive thousands of loan applications. Manually checking each applicant is time-consuming and risky.

The objective of this project is to build an ML model that can automatically assess customer risk and assign a suitable approval category.

---

## Dataset Used
The dataset was provided in two Excel files:

- `case_study1.xlsx`
- `case_study2.xlsx`

Both datasets were cleaned and merged using `PROSPECTID`.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Statistical Feature Selection

---

## Project Workflow

### 1. Data Cleaning
- Removed null values
- Removed invalid values (`-99999`)
- Removed highly missing columns
- Merged datasets

### 2. Feature Selection

#### Categorical Features:
Used **Chi-Square Test**

#### Numerical Features:
Used **VIF (Variance Inflation Factor)** to remove multicollinearity

#### Numerical Importance:
Used **ANOVA Test**

### 3. Feature Engineering
- Label Encoding
- One-Hot Encoding
- Standard Scaling (selected columns)

### 4. Model Building
Trained and compared:

- Random Forest Classifier
- Decision Tree Classifier
- XGBoost Classifier

### 5. Hyperparameter Tuning
Used **GridSearchCV** on XGBoost model.

Best Parameters:

```python
{
 'learning_rate': 0.2,
 'max_depth': 3,
 'n_estimators': 200
}
