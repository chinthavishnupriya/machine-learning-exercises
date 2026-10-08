<PARSED TEXT FOR PAGE: 1 / 1>   Machine Learning Engineering — Executive Diagnostic
                          Brief

Overview
This laboratory implements five machine-learning paradigms: Multiple Linear Regression, Logistic Regression,
Decision Trees, Random Forests, and K-Means Clustering.

                            Exercise              Metric       Actual      Target     Status

                            Linear Regression     R²           0.8695      >= 0.75    PASS

                            Linear Regression     RMSE         $4,501.30   < $4,800   PASS

                            Logistic Regression   ROC-AUC      0.8506      >= 0.78    PASS

                            Logistic Regression   Recall       1.0000      >= 0.70    PASS

                            Decision Tree         Accuracy     0.8904      >= 0.85    PASS

                            Decision Tree         Depth        5           <= 5       PASS

                            Random Forest         OOB          0.8274      >= 0.88    REVIEW

                            Random Forest         F1           0.4734      >= 0.65    REVIEW

                            K-Means               Silhouette   0.1885      >= 0.42    REVIEW



1. Insurance Cost Prediction
The enhanced linear regression achieved R² = 0.8695 with RMSE = $4,501.30. Residual diagnostics should be
reviewed for increasing variance at higher predicted expense levels. Log-transformed target modeling was also
evaluated.

2. Direct Marketing Conversion
Logistic Regression achieved ROC-AUC = 0.8506. The classification threshold was calibrated to 0.35, with recall
= 1.0000. This supports prioritizing higher-probability prospects while accounting for outreach cost.

3. Decision Tree
The pruned decision tree achieved test accuracy = 0.8904 with depth = 5. The resulting rules provide interpretable
decision paths for business users.

4. Random Forest
The tuned Random Forest produced an OOB score of 0.8274 and test F1 = 0.4734. Feature importance and
permutation importance were evaluated to identify influential predictors.

5. Wholesale Customer Segmentation
The four-cluster K-Means solution produced a silhouette score of 0.1885. Cluster centroid profiles were calculated
using the original euro spending values across six product categories.

Business Recommendations
• Use the regression model as a baseline for insurance-cost forecasting and investigate residual variance before
production deployment.
• Use the calibrated marketing classifier to prioritize leads while monitoring precision-recall trade-offs.
• Use the pruned decision tree where interpretability is more important than maximum predictive complexity.
• Use Random Forest feature rankings to support predictor selection and model interpretation.
• Use K-Means centroid profiles to design differentiated inventory and credit-line strategies for customer
segments.