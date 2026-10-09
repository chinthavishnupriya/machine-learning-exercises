# Lab Series 01 — Benchmark Status

The supplied lab guide requires the notebook and exported artifacts, with quantitative acceptance targets for all five exercises. fileciteturn40file1

## Corrections applied

- Exercise 1: fixed the enhanced raw-charge prediction artifact so the later log1p benchmark does not overwrite the saved test split.
- Exercise 2: fixed Recall@0.35 so the acceptance CSV records the numeric recall rather than a Boolean expression.
- Exercise 4: corrected dataset selection to use the full `bank-full.csv` and included `pdays`, which the guide explicitly identifies in its Random Forest feature-importance expectation. fileciteturn40file6
- The corrected notebook clears stale execution outputs and must be rerun from top to bottom.

## Previously observed results

| Exercise | Metric | Previous result | Target | Status |
|---|---:|---:|---:|---|
| 1 — Linear Regression | R² | 0.7836 | ≥ 0.75 | Pass |
| 1 — Linear Regression | RMSE | 5796.28 | < 4800 | Fail |
| 2 — Logistic Regression | ROC-AUC | 0.8506 | ≥ 0.78 | Pass |
| 2 — Logistic Regression | Recall@0.35 | Boolean value | ≥ 0.70 | Calculation bug |
| 3 — Decision Tree | Accuracy | 0.8904 | ≥ 0.85 | Pass |
| 3 — Decision Tree | Depth | 5 | ≤ 5 | Pass |
| 4 — Random Forest | OOB | 0.8947 | ≥ 0.88 | Pass |
| 4 — Random Forest | F1 | 0.3243 | ≥ 0.65 | Fail |
| 5 — K-Means | Silhouette@k4 | 0.1885 | ≥ 0.42 | Fail |

The guide specifically requires log1p followed by StandardScaler for Exercise 5, so the 0.1885 result should not be replaced with a different preprocessing method merely to force the benchmark to pass. fileciteturn40file3

**Final status: corrected notebook uploaded; final benchmark results still require a fresh top-to-bottom execution.**
