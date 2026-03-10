#  Fraud Detection in Financial Transactions

##  Project Overview
The objective of this project is to develop a robust Machine Learning system to detect fraudulent financial transactions. Using a highly imbalanced dataset (nearly 2M samples, <0.1% fraud), I progressed from a simple baseline to a sophisticated ensemble model combined with advanced feature engineering.

##  Key Achievements
* **97.6% Reduction in False Positives:** Slashed false alarms from over 100,000 to just **54** in the test set.
* **Maximum Security:** Achieved a **1.00 Recall**, identifying virtually all fraudulent transactions.
* **Business Impact:** High precision (0.97) ensures minimal customer friction while maintaining top-tier security.

##  Tech Stack
* **Language:** Python
* **Libraries:** Scikit-Learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn
* **Techniques:** Class Imbalance Handling (`class_weight`, `scale_pos_weight`), Pipeline construction, Feature Engineering, Ensemble Learning.

##  Model Evolution

| Model Stage | Model Type | Precision | Recall | F1-Score | False Positives |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Baseline** | Logistic Regression | 0.02 | 0.93 | 0.04 | 101,516 |
| **Intermediate** | XGBoost (Raw Data) | 0.51 | 0.98 | 0.67 | 2,322 |
| **Final** | **Random Forest (Enhanced)** | **0.97** | **1.00** | **0.98** | **54** |

##  The Winning Strategy: Feature Engineering
The breakthrough came from moving beyond raw data. I engineered three domain-specific features that exposed the mathematical logic behind fraud:

1. **`errorBalanceOrig`**: Captures discrepancies where the transaction amount doesn't match the origin account's balance shift.
2. **`errorBalanceDest`**: Identifies inconsistencies in how funds arrive at the destination.
3. **`isZeroAfter`**: A binary flag for accounts that were completely emptied—a common signature of fraudulent behavior.

These features provided such a strong signal that even a standard Random Forest outperformed complex gradient boosting models (XGBoost) in terms of precision.

##  Conclusion
The project demonstrates that **domain knowledge and feature engineering are often more impactful than model complexity**. By explicitly defining the "logic of fraud" through math-based features, I created a system that is both highly secure and operationally efficient.

---
*Developed as part of my Data Science Portfolio.*
