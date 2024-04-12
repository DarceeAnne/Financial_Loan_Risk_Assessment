# Financial Loan Risk Assessment

## Overview
This group project was developed with the goal of assessing financial loan risks using a dataset sourced from Kaggle. This dataset includes fictional data, consisting of approximately 32,000 records and 12 columns, where each row represents one loan record for one client.

## Data Source
- **Source:** [Kaggle - Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset/data)
- **Rows:** 32,000
- **Columns:** 12

## Data Preparation
### Cleaning
- Removed duplicate rows.
- Deleted age values greater than 100.
- Removed employment length values over 80 years.
- Dropped rows with missing values (NaNs).
- Excluded records where the interest rate equals 0%.

### Transformations
- Performed one-hot and label encoding on categorical data.
- Encoded `cb_person_default_on_file` with Y/N to 0/1.
- Transformed `loan_grade` from A to E.
- One-hot encoded `person_home_ownership` categories (Own, Rent, Mortgage).
- Encoded various `loan_intent`.

### Train/Test Split and Scaling
- Split data into training and testing sets with a test size of 20% and a random state of 0.
- Applied MinMaxScaler for normalization.

## Models Tested
### Classification Models
#### Targets:
- **Loan Status:** Identified profiles of clients more or less likely to default.
- **cb_person_default_on_file:** Profiled historically defaulting clients.

### Regression Models
#### Target:
- **Loan Amount:** Explored the association of loan amount with other numerical indicators.

### Model Selection
- Employed a weighted average F1 Score for classification models.
- Used weighted average R2 Score for regression models.
- Selected models include KNN, Decision Tree, Logistic Regression, Bagging & Pasting, Random Forest, Ada Boosting, and Gradient Boosting.

## Key Findings
### Application: Loan Status Target
#### Low Default Risk Profile
- Higher income, lack of previous defaults, home mortgage, and homeownership.

#### High Default Risk Profile
- Higher loan percentage of income, renters, previous defaults, and higher interest rates.

### Application: Loan Amount
- Developed targeted loan products and marketing strategies based on customer segmentation by age, income, and loan reason.
- Formulated strategies for interest rate assessments based on loan amounts.

## Conclusion
The project successfully implemented multiple machine learning models to assess and predict financial loan risks. The Random Forest model showed the highest accuracy in predicting loan amounts, while the Random Patches and Gradient Boosting models excelled in the loan status classification.

## Contributors
- [Michael Elbaz](https://www.linkedin.com/in/michael-elbaz/)
- [Adriana Brazon](https://www.linkedin.com/in/adriana-brazon/)
- [Gloria Lagrand](https://www.linkedin.com/in/gloria-lagrand-a35759102/)
- [Darcee Caron](https://www.linkedin.com/in/darceecarondataanalystpythonsqlpowerbi/)




