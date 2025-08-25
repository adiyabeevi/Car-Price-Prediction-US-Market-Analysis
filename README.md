# Car-Price-Prediction-US-Market-Analysis

## 📌 Project Overview
A Chinese automobile company aspires to enter the US market by setting up local manufacturing and competing with established US and European brands.  
The company contracted a consulting firm to understand the **factors affecting car prices** in the American market.  

This project builds **machine learning regression models** to predict car prices based on various car attributes and identifies the most significant factors that influence pricing.

---

## 🎯 Business Goal
- Predict the **price of cars** accurately.  
- Understand **which variables drive pricing** in the US market.  
- Provide insights to help the company adjust **design, features, and strategy** for market entry.  

---

## 🗂 Dataset
- **File:** `CarPrice_Assignment.csv`  
- **Rows:** 205 cars  
- **Columns:** 26 features including  
  - Car symboling, fuel type, aspiration  
  - Number of doors, body style, drive wheel  
  - Engine size, horsepower, curb weight, fuel system, etc.  
- **Target variable:** `price`

---

## ⚙️ Methodology
1. **Loading & Preprocessing**
   - Dropped irrelevant columns (`car_ID`, `CarName` text).
   - Separated numerical & categorical features.
   - Missing values handled with median/mode imputation.
   - Applied **StandardScaler** for numeric features and **OneHotEncoder** for categorical.

2. **Models Implemented**
   - Linear Regression  
   - Decision Tree Regressor  
   - Random Forest Regressor  
   - Gradient Boosting Regressor  
   - Support Vector Regressor (SVR)  

3. **Evaluation Metrics**
   - R² (Coefficient of Determination)  
   - Mean Squared Error (MSE)  
   - Mean Absolute Error (MAE)  

4. **Feature Importance**
   - Native importance (tree models).  
   - Permutation importance (model-agnostic).  

5. **Hyperparameter Tuning**
   - Used GridSearchCV for Random Forest.  
   - Compared tuned vs baseline models.  

---

## 📊 Results

### Model Comparison (Test Set)
| Model              | R²    | MSE       | MAE   |
|--------------------|-------|-----------|-------|
| Linear Regression  | ~0.xx | …         | …     |
| Decision Tree      | ~0.xx | …         | …     |
| Random Forest      | ~0.94 | …         | …     |
| Gradient Boosting  | ~0.xx | …         | …     |
| SVR                | ~0.xx | …         | …     |
| **Random Forest (Tuned)** | **0.957** | **3.37M** | **1280** |

*(Fill in the actual values from your notebook for Linear, Decision Tree, etc.)*

### Key Feature Drivers
- **Engine size & horsepower** – biggest impact on price.  
- **Car body type & brand** – strong segmentation effect.  
- **Curb weight** – correlates with build quality and segment.  
- **Fuel type/system** – premium fuels/engines priced higher.  

---

## ✅ Conclusion
- **Random Forest (Tuned)** was the best performing model, explaining **95.7% of price variance** with an average prediction error of only **$1,280**.  
- The model is both **accurate and interpretable**, making it suitable for pricing strategy decisions.  
- Insights can guide **design choices, market positioning, and feature adjustments** for successful entry into the US automobile market.

---

## 📂 Project Structure

├── CarPrice_Assignment.csv # Dataset
├── Car_Price_Prediction.ipynb # Jupyter Notebook with full code & analysis
├── best_car_price_model.pkl # (Optional) saved trained model
└── README.md # Project summary (README)
