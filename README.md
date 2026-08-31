# Credit Risk Prediction

A machine learning project that predicts whether a credit card customer is likely to default on their next payment.

## Dataset

The project uses the UCI Default of Credit Card Clients dataset, containing 30,000 customer records with demographic, credit limit, billing, payment and repayment history information.

## Project Workflow

1. **Data Understanding** – inspected structure, variables and data quality.
2. **Exploratory Data Analysis** – investigated default rates and relationships between customer behaviour and default.
3. **Feature Engineering** – created features summarising billing, payments, credit utilisation and repayment delays.
4. **Model Training** – compared Logistic Regression, Random Forest and HistGradientBoosting.
5. **Model Evaluation** – evaluated the selected model using classification metrics, a confusion matrix and ROC curve.

## Model Results

| Model | Accuracy | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|
| HistGradientBoosting | 0.817 | 0.366 | 0.470 | 0.778 |
| Random Forest | 0.812 | 0.369 | 0.464 | 0.758 |
| Logistic Regression | 0.808 | 0.292 | 0.402 | 0.742 |

HistGradientBoosting achieved the strongest overall performance with a ROC-AUC of **0.778**.

The final model correctly identified 486 defaults but missed 841, indicating that improving recall would be an important area for future development.

## Engineered Features

- `AVG_BILL_AMT` – average monthly bill
- `AVG_PAY_AMT` – average monthly payment
- `CREDIT_UTIL` – average bill relative to credit limit
- `DELAY_COUNT` – number of months with delayed payments
- `MAX_DELAY` – worst repayment delay

## Tools

- Python
- pandas
- NumPy
- scikit-learn
- Matplotlib
- Jupyter

## Future Improvements

Potential improvements include threshold tuning, class imbalance techniques and hyperparameter optimisation.