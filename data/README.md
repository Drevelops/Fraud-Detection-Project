# Data Sources

## Credit Card Fraud Detection Dataset

**Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

**Description**: European cardholders transactions over 2 days in September 2013

**Size**: 284,807 transactions (~150MB CSV file)

**Features**:
- **Time**: Number of seconds elapsed between each transaction and the first transaction
- **V1-V28**: Anonymized features (PCA transformed for privacy)
- **Amount**: Transaction amount
- **Class**: Target variable (1 = fraud, 0 = legitimate)

## Data Usage

**Original Dataset**: `creditcard.csv` (not included due to size - 150MB)

**Processed Files**:
- `fraud_transactions.csv`: Main dataset with calculated fields (hour_of_day, amount_bracket, time_period)
- `hourly_fraud_summary.csv`: Pre-aggregated hourly statistics
- `amount_fraud_summary.csv`: Pre-aggregated amount bracket analysis

## How to Reproduce

1. Download original dataset from Kaggle link above
2. Place in this directory as `creditcard.csv`
3. Run the data processing notebook to generate derived files

## Data Quality Notes

- No missing values in original dataset
- Highly imbalanced: 0.173% fraud rate (492 fraudulent out of 284,807 total)
- V-features are anonymized for privacy protection
- Time represents seconds since first transaction (not actual timestamps)