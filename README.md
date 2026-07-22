# 🏠 California Housing Price Prediction: Model Comparison

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

An extension of a linear regression baseline project, comparing three different regression models to predict median house prices across California districts using structured feature scaling and evaluation metrics.

---

## 📌 Dataset Overview

- **Source:** California Housing Dataset (built-in `scikit-learn`)
- **Volume:** 20,640 district records
- **Features:** 8 numerical attributes (*MedInc*, *HouseAge*, *AveRooms*, *Latitude*, *Longitude*, etc.)

---

## ⚙️ Methodology & Pipeline

1. **Feature Scaling:** Applied `StandardScaler` to ensure uniform feature weight distribution.
2. **Train/Test Split:** Data partitioned into **80% Training** and **20% Testing** subsets.
3. **Model Evaluation:** Evaluated algorithms using Root Mean Squared Error (**RMSE**) and Coefficient of Determination (**R² Score**):
   - Linear Regression
   - Ridge Regression
   - Decision Tree Regressor

---

## 📊 Results & Performance Comparison

| Model | RMSE | R² Score | Status |
| :--- | :---: | :---: | :---: |
| **Linear Regression** | `0.7460` | `0.5758` | Baseline |
| **Ridge Regression** | `0.7460` | `0.5758` | Regularized |
| **Decision Tree Regressor** | **`0.7270`** | **`0.5997`** | 🏆 **Best Performer** |

> 🏆 **Best Model:** **Decision Tree Regressor** achieved the lowest RMSE (`0.7270`) and highest R² Score (`0.5997`) on unseen test data.

---

## 💡 Key Insights

- **Baseline Stability:** Ridge Regression produced results nearly identical to Linear Regression, indicating negligible overfitting in the baseline model.
- **Non-Linear Relationships:** The Decision Tree captured complex non-linear feature interactions significantly better than linear models.
- **Generalization:** Train/Test comparisons confirmed that the Decision Tree maintained good generalization without severe overfitting.

---

## 🛠️ Tools & Libraries Used

- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** `scikit-learn`
- **Visualization:** Matplotlib

---

## 🚀 Limitations & Next Steps

- **Prediction Banding:** Output shows subtle step-like banding typical of single decision trees. Implementing **Random Forest** or **XGBoost** could smooth predictions and improve performance.
- **Hyperparameter Tuning:** Ridge `alpha` was manually defined; systematic tuning via `GridSearchCV` is recommended for future iterations.

---

## 📂 Repository Artifacts

- `AI_ML_Task2_Model_Comparison.ipynb` — *Full Jupyter Notebook containing dataset processing, modeling, and evaluations.*
- `Task2_Report.pdf` — *Exported analysis report detailing methodology, benchmark comparisons, and conclusions.*
