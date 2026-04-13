# RP-Diag: Credit Risk Model Complexity Audit

Diagnostic tool using Sparse Random Projections to detect
feature redundancy in credit risk models.

## Motivation
Over-parameterized PD models pose stability risks under
Basel IRB and IFRS 9 model validation frameworks.
This tool quantifies the effective dimensionality of a
credit dataset and flags redundancy risk.

## Dataset
Home Credit Default Risk (Kaggle)
- 300k samples, 122 features
- Binary classification: loan default prediction
- Sample used: 50,000 rows

## Key Results
- Intrinsic dimensions: 50 / 59 (post-preprocessing)
- Redundancy ratio: 15.3%
- Baseline AUC: 0.7251
- Regulatory flag: PASS — Well-calibrated dimensionality

## Methods
- Sparse Random Projection (sklearn)
- Ensemble averaging (n=20) for stable AUC estimation
- Logistic Regression baseline (class_weight='balanced')

## How to Run
1. Download application_train.csv from Kaggle:
   kaggle competitions download -c home-credit-default-risk
   -f application_train.csv -p data/
2. conda activate credit-rp
3. jupyter notebook
4. Run all cells in notebook.ipynb

## Files
- notebook.ipynb — main analysis
- requirements.txt — dependencies
- CLAUDE.md — project instructions for Claude Code
