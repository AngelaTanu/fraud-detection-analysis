# Fraud Detection Analysis

Exploratory data analysis identifying patterns that distinguish 
fraudulent transactions from legitimate ones, using a real-world 
credit card transaction dataset (284,807 transactions, 31 features).

## Business Question
Can we identify patterns that distinguish fraudulent transactions 
from legitimate ones, and what would a business analyst flag as a 
risk signal?

## Tools Used
- Python (pandas, numpy)
- Matplotlib / Seaborn
- SQL (equivalent queries included for key findings)
- Jupyter Notebook

## Approach
1. **Data Cleaning** — removed duplicate rows, checked for missing values
2. **Tier 1: Understand the dataset** — class imbalance, transaction timing
3. **Tier 2: Compare fraud vs. legitimate transactions** — amount patterns
4. **Tier 3: Timing patterns** — hour-of-day and burst analysis
5. **Tier 4: Deeper patterns** — feature correlation with fraud
6. **SQL equivalents** — key pandas findings translated into SQL queries
7. **Model concepts** — discussion of why accuracy is misleading for 
   imbalanced fraud data

## Key Findings
- **Class imbalance**: Fraud makes up only 0.17% of transactions 
  (473 of 283,726), meaning accuracy alone is a misleading metric — 
  a model predicting "not fraud" every time would still be 99.83% accurate.
- **Timing patterns**: Transaction volume follows a clear daily cycle, 
  with fraud not evenly distributed across time.
- **Top correlates**: V17, V14, V12, and V10 showed the strongest 
  correlation with fraudulent transactions.

## What I'd tell a fraud/risk team
Flag transactions where V17, V14, V12, or V10 fall outside typical 
ranges, and prioritize precision/recall over raw accuracy when 
evaluating any fraud detection model.

## Files
- `fraud_detection_analysis_PROJECT.ipynb` — full analysis notebook

## Author
Angie Mutanu
