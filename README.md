In this credit card fraud detection task, I tested four versions of the XGBoost Random Forest (XGBRF) model, focusing on the impact of resampling and parameter tuning techniques.

The baseline model achieved the highest precision (96.3%) and F1-score (87.8%), while maintaining strong specificity (99.99%) and a respectable recall (80.6%). This indicates it’s highly confident when flagging fraud but may miss a small portion of fraudulent transactions.

The tuned version of XGBRF performed similarly, with only a slight drop in recall and F1, suggesting limited gains from hyperparameter optimization in this setup.

On the other hand, resampled models (SMOTE and SMOTEENN) significantly improved recall to ~89.8%, meaning more frauds were caught — but at the cost of precision (down to 17.6% and 16.3%, respectively) and a sharp increase in false positives. While these versions may reduce missed fraud cases, they increase the burden of false alarms, which may be costly in real-world applications.

Key Insight:
If minimizing false positives is critical (e.g., to reduce unnecessary customer alerts), the baseline XGBRF offers the best trade-off. If maximizing fraud detection is the top priority regardless of false positives, then SMOTE-based models are worth considering — especially in hybrid systems with human-in-the-loop review.

link to dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data
