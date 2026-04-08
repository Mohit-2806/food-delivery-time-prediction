# 🚚 Food Delivery Time Prediction

A machine learning project to predict restaurant-to-customer delivery time using real-world logistics data.

## 📌 Overview
This project builds and evaluates multiple regression models to estimate food delivery time based on factors such as location, traffic, weather, and order timing.

The goal is to simulate a real-world logistics problem and demonstrate end-to-end ML workflow: data cleaning, feature engineering, model comparison, and optimization.

---

## 📊 Dataset
- Source: Kaggle  
- Training samples: 45,593  
- Test samples: 11,399  
- Target variable: `Time_taken(min)` (10–54 minutes)

---

## ⚙️ Approach

### 1. Data Cleaning
- Standardized inconsistent text values and handled missing data  
- Converted target variable from string format to numeric  
- Fixed formatting issues in categorical columns (e.g., weather conditions)

---

### 2. Feature Engineering
Created meaningful features to improve model performance:

- **Time-based features**
  - Order hour, pickup hour  
  - Pickup delay (in minutes)  
  - Rush hour indicator  
  - Day, month, weekday, weekend flag  

- **Distance feature**
  - Computed using Haversine formula from restaurant to delivery location  

- **Categorical encoding**
  - Ordinal encoding for traffic density, weather, and city type  
  - Label encoding for remaining categorical variables  

---

### 3. Data Preparation
- Train-test split: 80/20  
- Applied feature scaling (StandardScaler) where required  

---

### 4. Model Comparison
Trained and evaluated multiple models:

- Linear Regression  
- Decision Tree  
- Random Forest  
- K-Nearest Neighbors  
- XGBoost  

Evaluation metrics:
- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  
- R² Score  

---

## 🏆 Results

| Model           | Performance |
|----------------|------------|
| XGBoost (Tuned) | **Best** |

- **R² Score:** 0.81  
- **MAE:** 3.23 minutes  
- **RMSE:** 4.04 minutes  

The XGBoost model significantly outperformed baseline models by capturing non-linear relationships in the data.

---

## 💡 Key Insights
- Delivery time is strongly influenced by **distance and traffic conditions**  
- **Pickup delay** is a critical hidden factor affecting final delivery time  
- Feature engineering contributed more to performance improvement than model complexity alone  

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib  

---

## ▶️ How to Run
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Run all cells  

---

## 🚀 Future Improvements
- Hyperparameter tuning using GridSearch/Optuna  
- Incorporating real-time traffic APIs  
- Trying advanced models (LightGBM, CatBoost)  
- Deploying as a prediction API  

---

## 👤 Author
Mohit Ramrakhyani
