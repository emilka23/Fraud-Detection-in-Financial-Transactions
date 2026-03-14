#  Fraud Detection in Financial Transactions

##  Project Overview
The goal of this project was to build a high-performance machine learning system capable of detecting fraudulent financial transactions in a highly imbalanced dataset. The project demonstrates the full data science lifecycle, from exploratory data analysis and domain-specific feature engineering to the comparative evaluation of multiple classification algorithms.

## Key Achievements
* **Elite Accuracy:** Achieved a **Recall of 0.996** and **Precision of 0.999** using the final Random Forest model.
* **Precision Engineering:** Successfully reduced False Positives to near-zero, ensuring a frictionless experience for legitimate customers.
* **Domain Feature Engineering:** Identified and implemented key accounting features (`errorBalance`, `isZeroAfter`) that became the primary drivers of model performance.
* **Baseline Evolution:** Systematically improved model precision from **0.03** (Logistic Regression) to **0.99** (Random Forest).

##  Tech Stack
* **Language:** Python
* **Libraries:** Scikit-Learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn
* **Techniques:** Class Imbalance Handling , Pipeline construction, Feature Engineering.

##  Model Evolution

| Model | Recall (Fraud) | Precision (Fraud) | Status |
| :--- | :---: | :---: | :--- |
| **Logistic Regression** | 0.99 | 0.03 | Baseline |
| **Random Forest** | **0.996** | **0.999** | **Winner (Production Ready)** |

##  The Winning Strategy: Feature Engineering
The breakthrough came from moving beyond raw data. I engineered three domain-specific features that exposed the mathematical logic behind fraud:

1. **`errorBalanceOrig`**: Captures discrepancies where the transaction amount doesn't match the origin account's balance shift.
2. **`errorBalanceDest`**: Identifies inconsistencies in how funds arrive at the destination.
3. **`isZeroAfter`**: A binary flag for accounts that were completely emptied—a common signature of fraudulent behavior.

These features consistently ranked at the top of the **Feature Importance** plots, proving that domain knowledge is often more impactful than algorithm complexity.

##  Conclusion
The project concludes that a **Random Forest** classifier, supported by targeted **Feature Engineering**, is an ideal solution for real-time fraud detection. The final model is ready for production deployment, offering maximum security with virtually zero operational waste (False Positives).

---
** Dataset: **  [Kaggle - Fraud Detection Dataset] (https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)
*Developed as part of my Data Science Portfolio.*
