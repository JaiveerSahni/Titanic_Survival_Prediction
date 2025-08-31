# 🚢 Titanic Survival Prediction

##  Project Overview
A classic binary classification task using the Titanic dataset from Kaggle: **predict whether a passenger survived or not**. The notebook walks through data exploration, feature engineering, model training, evaluation, and comparison.

##  Table of Contents
1. [Dataset](#dataset)  
2. [Features Engineered](#features-engineered)  
3. [Modeling Workflow](#modeling-workflow)  
4. [Model Comparison & Evaluation](#model-comparison--evaluation)  
5. [Results & Interpretation](#results--interpretation)  
6. [Future Improvements](#future-improvements)  
7. [Project Structure](#project-structure)

---

##  Dataset
- Source: “Titanic – Machine Learning from Disaster” on Kaggle.  
- Commonly used for learning classification with real-world data challenges like missing values and categorical features. :contentReference[oaicite:0]{index=0}  

The dataset includes features such as `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, among others. The target variable is `Survived` (0 = No, 1 = Yes).

---

##  Features Engineered
- **Standard Features**: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked.  
- **New Features**:
- **FamilySize** = SibSp + Parch + 1: captures traveling with family.  

These features help capture survival tendencies, such as higher survival rates for women, children, and small families. 

---

##  Modeling Workflow
1. **Preprocessing**  
    - Handle missing values (e.g., fill median Age, common Embarked values).  
    - Encode categorical variables using one-hot encoding.  
    - Scale numeric features if required (especially for certain models).

2. **Model Training**  
    - Baseline: Logistic Regression  
    - Other models: Decision Tree, Random Forest, Gradient Boosting (e.g., XGBoost)  

---

##  Model Comparison & Evaluation
Metrics used for model evaluation:
- **Accuracy**: overall correctness  
- **Precision**, **Recall**, **F1 Score**: especially recall for identifying survivors  
- **ROC-AUC**: model’s ability to distinguish between survivors and non-survivors across thresholds  

Visuals include:
- Confusion Matrix  
- ROC Curve for each model  
- Bar plots comparing metrics across models

---

##  Results & Interpretation
- Logistic regression serves as an interpretable baseline.  
- Random Forest / Gradient Boosting typically outperform in accuracy and AUC.  
- ROC-AUC provides a strong summary of model separation capacity (higher AUC = better).  
- Feature importances highlight key predictors like `Sex`, `Pclass`, and `FamilySize`.

---

##  Future Improvements
- Try **XGBoost**, **LightGBM**, or **CatBoost** for performance gains.  
- Perform **feature engineering** such as extracting titles from `Name` or cabin decks.  
- Deploy a prediction interface using Flask or Streamlit.  
- Conduct deeper hyperparameter optimization for better generalization.

---


