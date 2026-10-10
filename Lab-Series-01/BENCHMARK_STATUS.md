# Lab Series 01 — Verification Status

## Current status

The five exercise sections have been implemented and run in Google Colab. The lab is **not yet fully passing all quantitative acceptance targets**.

## Latest values visible in the user's Colab screenshots

| Exercise | Metric | Latest observed value | Target | Status |
|---|---|---:|---:|---|
| Exercise 2 — Logistic Regression | ROC-AUC | 0.8645 | >= 0.78 | Pass |
| Exercise 2 — Logistic Regression | Recall at threshold 0.35 | 0.8487 | >= 0.70 | Pass |
| Exercise 4 — Random Forest | OOB score | 0.9030 | >= 0.88 | Pass |
| Exercise 4 — Random Forest | F1 | 0.6162 | >= 0.65 | Not met |
| Exercise 5 — K-Means | Silhouette at k=4 | 0.1885 | >= 0.42 | Not met |

Exercise 1 and Exercise 3 values must be copied from their latest successful output cells before a final all-exercise acceptance CSV is published. Earlier summary values in the repository may be stale and must not be treated as the final run.

## Remaining work

1. Re-run the notebook from a clean runtime and ensure every cell completes in order.
2. Fix any cell errors (including the permutation-importance sparse-matrix input, by converting the transformed test matrix to a dense array only for that diagnostic if memory permits).
3. Investigate Random Forest F1 with validation-only threshold selection and model tuning; retain the measured test result even if it remains below 0.65.
4. Keep the lab-required K-Means preprocessing (log1p followed by StandardScaler) and report the actual silhouette score. Do not change the score manually to meet the target.
5. Export the final prediction CSVs, centroids, cluster assignments, and acceptance summary from the same final run.
6. Save the executed notebook successfully in Drive, then upload that exact notebook and the generated artifacts to this repository.

Do not mark all checks as passed unless the final executed notebook demonstrates that result.
