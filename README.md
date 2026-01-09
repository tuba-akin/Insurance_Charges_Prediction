# Insurance Charges Analytics & Premium Estimator (Power BI + ML)

This repository contains an end-to-end portfolio project focused on understanding and estimating medical insurance charges.  
It includes:
- A **Power BI dashboard** (3 pages) for KPI reporting, driver analysis, and an interactive **what-if premium estimator**
- A **Colab/Jupyter notebook** that trains baseline ML models (including **Linear Regression**) and supports model interpretation

---

## Dashboard Overview (Power BI)

### Page 1 — Overview & KPIs
- Key metrics (policy count, average charges, smoker rate, average BMI)
- Distributions and comparisons across region, gender, BMI categories, and smoking status

### Page 2 — Drivers & Distribution
- Charge distribution (binned)
- Cost concentration (e.g., smoker cost share, top 10% cost share)
- Driver exploration using **Key Influencers** and **Decomposition Tree**

### Page 3 — ML Estimator (What-if)
Users select:
- Age, BMI, children
- Sex, smoker status, region  
…and the report returns an **Estimated Premium** using Linear Regression coefficients.
A contributions panel explains how each input affects the final estimate.

---

## Dataset
The dataset is included in:
- `data/insurance.csv`

Columns:
- `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`

---

## Notebook (Model Training)
Notebook location:
- `notebooks/Insurance_Charges_Prediction.ipynb`

The notebook:
- Loads and explores the dataset
- Applies preprocessing (one-hot encoding for categorical features)
- Trains baseline models (incl. Linear Regression)
- Evaluates performance using MAE / RMSE / R²
