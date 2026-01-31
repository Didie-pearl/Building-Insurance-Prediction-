#  Building Insurance Claim Prediction

##  Project Overview
Insurance companies in Nigeria face challenges in identifying high-risk buildings effectively. This project analyzes building data (dimension, age, type, location) to predict the probability of an insurance claim over a specific period.

The goal is to build a predictive model that allows the insurance company to optimize premiums and manage risk better.

## 📊 Key Findings & Insights
* **Size Matters:** The `Building_Dimension` was the #1 predictor of claims. Larger buildings are significantly higher risk.
* **Linear Relationships:** Simple linear models outperformed complex tree-based models, suggesting a direct correlation between risk factors (like size/age) and claims.
* **Building Type:** There is a clear risk progression from `Type 1` (Safe) to `Type 4` (High Risk).

##  Model Performance
I experimented with three algorithms: **Logistic Regression**, **Random Forest**, and **Gradient Boosting**.

| Model | ROC-AUC Score | Verdict |
| :--- | :--- | :--- |
| **Logistic Regression** | **0.72** |  **Best Model** |
| Gradient Boosting | 0.69 | Robust, but slightly overfit |
| Random Forest | 0.66 | Struggled with noise |

*Metric used: ROC-AUC (Area Under the Receiver Operating Characteristic Curve) due to class imbalance.*

##  Data Pipeline
1.  **Data Cleaning:** handled missing values in `Garden`, `Geo_Code`, and `Date_of_Occupancy`.
2.  **Outlier Engineering:** Log-transformed `Building_Dimension` to handle extreme values and capped `Building_Age`.
3.  **Feature Engineering:** Frequency encoded `Geo_Code` (Location) and mapped categorical variables.
4.  **Feature Selection:** Removed weak predictors (`Garden`, `Settlement`) to reduce noise.

##  Tech Stack
* **Python** (Pandas, NumPy)
* **Visualization** (Seaborn, Matplotlib)
* **Machine Learning** (Scikit-Learn)

##  Repository Structure
* `Notebook.ipynb`: The full analysis and modeling code.
* `insurance_claim_model.pkl`: The final trained model (ready for deployment).
* `requirements.txt`: Dependencies for reproducing the analysis.

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Building-Insurance-Prediction-Nigeria.git](https://github.com/YOUR_USERNAME/Building-Insurance-Prediction-Nigeria.git)
