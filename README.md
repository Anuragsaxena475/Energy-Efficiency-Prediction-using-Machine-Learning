
# 🔋 Energy Efficiency Prediction using Machine Learning

This repository presents a machine learning project that applies **data preprocessing**, **Random Forest Regression**, and **Gradient Boosting Regression** to predict the **Heating Load (Y1)** and **Cooling Load (Y2)** of buildings based on their architectural and environmental features.

## 📂 Dataset

The dataset used in this project is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/242/energy+efficiency). It contains **768 samples** and **10 numerical features**, representing different physical parameters of simulated buildings.

### 🔧 Features

| Column | Description                                   |
|--------|-----------------------------------------------|
| X1     | Relative Compactness                          |
| X2     | Surface Area                                  |
| X3     | Wall Area                                     |
| X4     | Roof Area                                     |
| X5     | Overall Height                                |
| X6     | Orientation (encoded as integers 2–5)         |
| X7     | Glazing Area                                  |
| X8     | Glazing Area Distribution (encoded as integers 0–5) |
| Y1     | Heating Load (target 1)                       |
| Y2     | Cooling Load (target 2)                       |

---

## 🧪 Objective

To build predictive models that estimate:
- `Y1`: **Heating Load**  
- `Y2`: **Cooling Load**

… based on the 8 input features (X1 to X8).

---

## 🛠️ Workflow

1. **Data Loading**
2. **Exploratory Data Analysis**
3. **Data Preprocessing**
   - Handled any missing/null values
   - Label encoding for categorical variables (X6 and X8)
   - Feature scaling using `StandardScaler`
4. **Model Training**
   - Random Forest Regression
   - Gradient Boosting Regression
5. **Model Evaluation**
   - Mean Squared Error (MSE)
   - Root Mean Squared Error (RMSE)
   - R² Score

---

## 🧠 Models & Results

### 🌳 Random Forest Regressor

**🔹 Heating Load (Y1):**
- **MSE:** 0.2409  
- **RMSE:** 0.4908  
- **R² Score:** 0.9977  

**🔹 Cooling Load (Y2):**
- **MSE:** 2.9341  
- **RMSE:** 1.7129  
- **R² Score:** 0.9683  

➡️ **Interpretation:**  
The Random Forest model performs exceptionally well, especially for predicting **Heating Load** with a very high R² score (~99.77%). Cooling Load prediction is also strong, though slightly less accurate than heating.

---

### 🌟 Gradient Boosting Regressor

**🔹 Heating Load (Y1):**
- **MSE:** 0.2653  
- **RMSE:** 0.5151  
- **R² Score:** 0.9975  

**🔹 Cooling Load (Y2):**
- **MSE:** 2.2898  
- **RMSE:** 1.5132  
- **R² Score:** 0.9753  

➡️ **Interpretation:**  
Gradient Boosting also performs extremely well. It slightly underperforms Random Forest for **Heating Load**, but **outperforms Random Forest** for **Cooling Load** with a higher R² and lower error.

---

## 📊 Model Comparison Summary

| Metric        | RF (Heating) | GBR (Heating) | RF (Cooling) | GBR (Cooling) |
|---------------|--------------|---------------|--------------|---------------|
| **MSE**       | 0.2409       | 0.2653        | 2.9341       | 2.2898        |
| **RMSE**      | 0.4908       | 0.5151        | 1.7129       | 1.5132        |
| **R² Score**  | 0.9977       | 0.9975        | 0.9683       | 0.9753        |

✅ Both models provide **high accuracy**. You can choose between them depending on whether you prioritize heating or cooling prediction performance.

---
## 📌 Requirements

- Python 
- pandas
- numpy
- scikit-learn
- matplotlib / seaborn

