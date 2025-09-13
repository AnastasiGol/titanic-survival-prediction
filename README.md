\# Titanic Survival Prediction



\## Overview

This project tackles the classic \*\*Kaggle Titanic Machine Learning Competition\*\*, aiming to predict whether a passenger survived the Titanic disaster based on features like \*\*age, sex, class, fare, and embarkation point\*\*.  



Through \*\*exploratory data analysis (EDA)\*\*, \*\*feature engineering\*\*, and multiple machine learning models, we achieve an \*\*84% accuracy\*\* on the test set using a \*\*Support Vector Classifier (SVC)\*\*.  

The final predictions are saved as a CSV file for Kaggle submission, scoring \*\*94.7%\*\* against the gender-based baseline comparison.  



---



\## Dataset

\- \*\*Source\*\*: Kaggle Titanic Dataset  

\- \*\*Train\*\*: 891 passengers (with survival labels)  

\- \*\*Test\*\*: 418 passengers (predictions required)  

\- \*\*Key Features\*\*: `PassengerId`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, `Embarked`  

\- \*\*Target\*\*: `Survived` (0 = No, 1 = Yes)  



Missing values (e.g., `Age`, `Cabin`, `Fare`) are handled via \*\*imputation and prediction\*\*.  



---



\## Approach



\### Exploratory Data Analysis (EDA)

\- \*\*Visualizations\*\*: Survival counts, correlations using Seaborn/Matplotlib.  

\- \*\*Insights\*\*: Women and higher-class passengers had higher survival rates.  



\### Data Preprocessing

\- Handle missing values (e.g., predict `Age` using a Random Forest regressor).  

\- Categorical encoding (One-Hot for `Sex` and `Embarked`).  

\- Feature engineering: Create new feature \*\*`Family = SibSp + Parch`\*\*.  

\- Scaling and imputation via \*\*scikit-learn Pipeline\*\*.  



\### Model Selection

\- Compared models: \*\*Random Forest, Gradient Boosting, Logistic Regression, SVC\*\*.  

\- \*\*Best model\*\*: \*\*SVC\*\* (84% accuracy on hold-out set).  



\### Evaluation

\- \*\*Metrics\*\*: Accuracy, Precision, Recall, F1-Score.  

\- Cross-validation approximated via \*\*train-test split (70/30)\*\*.  



---



