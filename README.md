# Credit-Default-Prediction-using-Machine-Learning
1. Introduction
This capstone project aims to build a classification model to predict customer defaults using financial and demographic data. The goal is to assist in early risk identification and improve lending strategies.

2. Data Source
Dataset: 2013-14_Filtered.csv

Target: default_ind (1 = default, 0 = no default)

3. Data Preprocessing
Dropped columns with >50% missing data.

Imputed missing values:

Categorical: Mode

Numerical: Median

Encoded categorical features with Label Encoding.

Addressed multicollinearity using VIF.

Scaled features using StandardScaler.

4. Handling Imbalanced Data
Applied SMOTE to balance class distribution.

5. Model Building
Tested the following algorithms:

Logistic Regression

Random Forest

XGBoost

Model selection used:

Cross-validation

Grid search for hyperparameter tuning

6. Evaluation Metrics
Confusion Matrix

Precision, Recall, F1-score

Precision-Recall Curve

 Optimal Threshold: 0.33
Chosen based on the best F1 Score: 0.9227

📊 Classification Report
Class	Precision	Recall	F1-Score	Support
0 (No Default)	1.00	1.00	1.00	80,108
1 (Default)	0.91	0.94	0.92	632
Accuracy			1.00	80,740
Macro Avg	0.96	0.97	0.96	80,740
Weighted Avg	1.00	1.00	1.00	80,740

🧮 Confusion Matrix
lua
Copy
Edit
[[80050    58]
 [   41   591]]
Interpretation:

True Negatives (80050): Correctly predicted non-defaulters

True Positives (591): Correctly predicted defaulters

False Positives (58): Incorrectly predicted defaulters

False Negatives (41): Missed defaulters


7. Results
Model		Precision	Recall	F1-score
XGBoost	0.91–1.00	0.94–1.00	0.92 (best F1)

Final Chosen Model: XGBoost — with high accuracy and strong balance of precision and recall, especially for identifying defaults (minority class).

