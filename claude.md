# CLAUDE.md

## Project Overview
Random Projection diagnostic tool for credit risk models.
Goal: Show how much a high-dimensional credit dataset can be
compressed using Sparse Random Projections while retaining
classification performance (AUC).
Final deliverable: a readable notebook.ipynb

## Language
All output must be in English.
This includes: markdown cells, plot labels, axis titles,
printed outputs, code comments, and take-home message.
No Chinese anywhere in the notebook.

## Environment
- conda env: credit-rp (Python 3.11)
- dependencies: see requirements.txt

## Data
- File: data/application_train.csv
- Source: Kaggle Home Credit Default Risk (kaggle username: johnzhenghuang)
- Download via Kaggle API if file not present
- Sample: 50,000 rows (random_state=42)
- Do NOT commit data to git

## Notebook Structure
7 sections, each with a markdown explanation cell + code cell(s):
0. Setup & Imports
1. Data Preprocessing
2. EDA
3. Baseline: Full-dimension Logistic Regression
4. Random Projection Experiment (Sparse RP, ensemble n=20)
5. Intrinsic Dimensionality Diagnosis
6. Final Visualization + Take-home Message

## Code Style
- Simple and readable — code will be presented and explained
- Each code cell max 30 lines
- English labels on all plots
- Markdown cells explain the "why", not just the "what"
- No redundant comments inside code
- Variable names should be self-explanatory

## Key Parameters
- sample_size = 50000
- test_size = 0.2
- random_state = 42
- n_ensemble = 20
- k_range = [2,3,4,5,8,10,15,20,25,30,40,50,60,70,85]
- threshold = 0.99 (99% of baseline AUC)
- class_weight = 'balanced'