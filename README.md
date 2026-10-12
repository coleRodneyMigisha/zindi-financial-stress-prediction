# Zindi Financial Stress Prediction

## Project Overview

This project addresses the Zindi Beginner Track: Financial Stress Prediction Challenge (September Edition).

The objective is to predict whether a customer is likely to experience financial or liquidity stress within the next 30 days, using features derived from their mobile money transaction behaviour over a six-month observation period.

## Dataset

The competition dataset contains 40,000 training records and 30,000 test records. Features include numerical and categorical information describing customer demographics and financial behaviour.

The competition data is not included in this repository. Please obtain it through the official competition platform and follow its data-use rules.

## Methodology

The workflow includes:

- Exploratory data analysis and data quality checks.
- Feature and target inspection.
- Five-fold stratified cross-validation.
- Comparison of Logistic Regression and LightGBM.
- Evaluation using ROC-AUC and Log Loss.
- Generation and validation of predicted probabilities for the test dataset.

## Validation Results

| Model | Mean ROC-AUC | Mean Log Loss |
|---|---:|---:|
| Logistic Regression | 0.7532 | 0.3750 |
| LightGBM | 0.8829 | 0.2790 |

These are reported cross-validation results. They may differ from the public leaderboard score.

## Public Leaderboard

- Public score: `0.683277301`

The score is recorded as returned by the competition platform. Its interpretation depends on the competition's official scoring formula.

## Project Structure

```text
zindi-financial-stress-prediction/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── 01_financial_stress_prediction.ipynb
├── src/
└── submissions/
```

## Reproducibility

The notebook documents the exploration, model evaluation, and submission workflow. Review its package requirements and execution instructions before reproducing the results.

## Limitations

- Validation performance may not fully represent the hidden test distribution.
- The public leaderboard evaluates only part of the test data.
- No improvement in leaderboard performance is guaranteed by additional feature engineering or model ensembling.

## Disclaimer

This project is for educational and machine learning practice. The predictions are model estimates and should not be treated as definitive financial assessments of individuals.
