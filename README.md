# Employee-Attrition-Prediction-Models
Machine learning project that predicts which employees are likely to leave a company, using the IBM HR Analytics Employee Attrition dataset (1,470 employees, about 16% attrition).

## Repository contents
| File | Description |
|---|---|
| Attrition_Model_Notebook.ipynb | Full model notebook (EDA, modelling, tuning, feature importance) |
| Evaluation_Report.docx | Model evaluation and comparison report |
| Business_Interpretation_Report.docx | Findings and recommendations for HR |
| outputs/ | Saved plots and metric tables |

## Approach
- Classification target:Attrition (Yes/No)
- Algorithms: Logistic Regression, Decision Tree, Random Forest, XGBoost
- Data split: 80/20 stratified train-test split
- Imbalance handling: class weighting
- Metrics:Accuracy, Precision, Recall, F1, ROC-AUC
- Improvement: 5-fold stratified cross-validation, GridSearchCV hyperparameter tuning, feature importance (Random Forest, XGBoost, Logistic Regression coefficients)
- Optional regression task: predicting JobSatisfaction (1-4) with Linear, Ridge, Random Forest and XGBoost regressors

## Key findings
- Logistic Regression gave the best ROC-AUC after tuning (about 0.81) and the highest recall.
- Overtime, monthly income, age, experience, business travel and stock options are the main attrition drivers.
- JobSatisfaction could not be predicted from the other HR fields (R² near zero).

## How to run (Google Colab)
1. Upload Attrition_Model_Notebook.ipynb to Google Colab.
2. Click Runtime > Run all.
3. The dataset downloads automatically; if it fails, you will be asked to upload the CSV.

## Dataset
IBM HR Analytics Employee Attrition: https://github.com/IBM/employee-attrition-aif360
