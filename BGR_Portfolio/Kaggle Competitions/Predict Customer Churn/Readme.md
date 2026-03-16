This competition goal is to Predict Customer Churn.

Given the input features, I added a RFM (Recency, Frequency, Monetary) analysis to study effect of tenure, active services and MonthlyCharges on Churn. 
Additionally, with the RFM metrics added to the dataset, I compare four models using 5-fold stratified cross-validation (ROC-AUC):

  - Logistic Regression – linear baseline
  - Random Forest – bagging ensemble
  - XGBoost – gradient boosting (boosted trees)
  - LightGBM – fast gradient boosting

XGBOOST is the best performing model, irrespective of using RFM features or not, athough the AUC was not very different compared to LightGBM.
Key RFM Insights
  - Recency (tenure): Customers with low tenure churn far more frequently — recent acquires are at highest risk.
  - Frequency (active services): Customers subscribed to fewer services have higher churn rates — low engagement is a warning sign.
  - Monetary (monthly charges): Higher charges combined with low tenure is a particularly risky combination.
  - "Lost" segment (low RFM score) has the highest churn rate; "Champions" have the lowest.
  - RFM features add measurable lift to tree-based models over the baseline features alone.


Link to the competition: https://www.kaggle.com/competitions/playground-series-s6e3/overview

Link to my submission: https://www.kaggle.com/code/ganapathybalajir/customer-churn-prediction-with-rfm-analysis

Leaderboard: https://www.kaggle.com/competitions/playground-series-s6e3/leaderboard
