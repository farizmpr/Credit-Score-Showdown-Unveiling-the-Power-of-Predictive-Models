# Credit Score Showdown: Unveiling the Power of Predictive Models
## Abstract
The banking industry's need for precise credit risk assessment is critical. This project explores the effectiveness of various predictive models in estimating credit risk based on a provided dataset. We analyze and compare the performances of a random forest model and logistic regression models enhanced with the Weight of Evidence (WOE) measure, considering both models with and without imbalance handling. Our findings aim to guide banks in selecting the most suitable model for credit scoring, balancing predictive accuracy with regulatory compliance requirements.
## Objectives
-  To compare the predictive accuracy of random forest and logistic regression models in credit scoring.
-  To enhance logistic regression with the Weight of Evidence (WOE) for improved prediction.
-  To evaluate model performances with a focus on handling imbalanced datasets.
-  To provide recommendations based on model performances and compliance with financial regulations.
## Methodology
The project employs a random forest model and logistic regression models, with a focus on interpretability and handling of imbalanced datasets. Preprocessing steps include variable analysis, handling missing values, outlier detection, and the application of WOE for variable transformation. The models are evaluated based on precision, recall, F1-score, and accuracy in predicting credit risk.
## Key Findings
-  The random forest model exhibited superior predictive accuracy (86%) but may face regulatory challenges due to its "black box" nature.
-  Logistic regression with WOE, despite lower accuracy (73% without imbalance handling, 56% with imbalance handling), offers transparency that aligns with regulatory standards.
-  Imbalance handling proved essential for achieving a balanced prediction between defaulters and non-defaulters.
## Recommendations
-  For environments with less stringent interpretability requirements, the random forest model is recommended due to its high accuracy.
-  Where regulatory compliance and model interpretability are crucial, logistic regression with WOE is advisable. Consideration of imbalance handling depends on the priority of balanced accuracy across classes.
-  Further analysis of influential variables and integration of comprehensive financial records are suggested to enhance model performance.
## Result
### Reference Categories

| Category                     | Reference Value |
|------------------------------|-----------------|
| COMPANY                      | Y               |
| MARITAL                      | 1               |
| MONTHS_IN_RESIDENCE          | >60             |
| MONTHS_IN_THE_JOB            | <0              |
| OCC_TYPE                     | 4.0             |
| PAYMENT_DAY                  | 25              |
| PERSONAL_MONTHLY_INCOME      | 845-1238.872    |
| PRODUCT                      | 7               |
| POSTAL_CODE                  | 2               |
| RESI_TYPE                    | 2               |
| STATE_RESI                   | SE              |
| EDUCATIONAL                  | 0.0             |
| AGE                          | >83             |

### Results for Logistic Regression with WOE

| Class        | Precision | Recall | F1-score | Support |
|--------------|-----------|--------|----------|---------|
| Bad Class (0) | 0.67      | 0      | 0        | 2,664   |
| Good Class (1)| 0.73      | 1.0    | 0.85     | 7,336   |
| **Accuracy**  |           |        | 0.73     | 10,000  |

### Results for Logistic Regression with WOE + Imbalance Handling

| Class        | Precision | Recall | F1-score | Support |
|--------------|-----------|--------|----------|---------|
| Bad Class (0) | 0.56      | 0.55   | 0.55     | 7,417   |
| Good Class (1)| 0.55      | 0.57   | 0.56     | 7,367   |
| **Accuracy**  |           |        | 0.56     | 14,784  |

### Comparative Analysis Results

| Models                           | Accuracy Rate | AUC  | GINI  |
|----------------------------------|---------------|------|-------|
| LogR: Imbalance handling         | 0.50          | 0.49 | -0.001|
| LogR: WOE                         | 0.73          | 0.60 | 0.19  |
| LogR: Imbalance handling, WOE    | 0.56          | 0.56 | 0.11  |
| Random Forest                    | 0.86          | 0.86 | 0.71  |
