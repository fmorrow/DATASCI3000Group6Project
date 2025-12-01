# DATASCI3000Group6Project

# Asteroid Diameter Prediction Project

## 📌 Project Overview
This project focuses on predicting **asteroid diameters** using orbital and physical characteristics collected from NASA/JPL datasets.  
Multiple machine learning regression models were trained and evaluated to determine which model best captures the relationship between asteroid properties and diameter size.

The project includes:
- Data cleaning & preprocessing
- Feature engineering
- Outlier detection and treatment
- Regression model training
- Performance comparison of ML models
- Ensemble learning using a stacking regressor

---

## 📊 Dataset
The dataset contains information about asteroid orbital dynamics and physical properties including:

### Features Used in Prediction:
- RMS
- Reflectivity (albedo)
- Diameter error
- Brightness
- Perihelion distance
- Aphelion distance
- Semi-major axis
- Orbital speed
- Orbit eccentricity
- MOID (Minimum Orbit Intersection Distance)

### Target Variable:
- `diameter`

---

## 🛠 Data Preprocessing
The following preprocessing steps were applied:

- Dropped irrelevant identifier columns (IDs, epoch fields, orbital metadata)
- Renamed columns for readability
- Handled missing values using:
  - Mean imputation for brightness
  - Median imputation for reflectivity and diameter error
- Removed outliers using the **IQR method**
- Encoded categorical variables using label encoding
- Applied **standard scaling** to numeric features
- Split dataset into:
  - 70% Training set
  - 20% Validation set
  - 10% Test set

---

## 🤖 Models Implemented

### Baseline Models:
- Linear Regression
- Ridge Regression
- Lasso Regression

### Tree-Based Models:
- Random Forest Regressor
- Extra Trees Regressor
- XGBoost
- CatBoost

### Neural Network:
- MLP Regressor

### Ensemble Model:
- Stacking Regressor (Random Forest + XGBoost + MLP → Ridge Meta-model)

---

## 🧪 Model Evaluation Metrics

Each model was evaluated using:
- **R² Score** — Measures goodness of fit
- **RMSE** — Measures prediction error magnitude

Metrics were computed on:
- Training set
- Validation set
- Test set (final evaluation)

---

## 🏆 Best Performing Model

Based on training and validation performance:
- The **Stacking Regressor** showed the strongest generalization performance.
- It combined the strengths of tree models and neural networks while reducing individual model biases.

---

## 📈 Visualization & Analysis

This project includes:
- Feature vs target regression plots
- Correlation heatmaps
- Feature importance charts from Random Forest
- Missing value analysis dashboards
- Outlier reporting tables

---

## 📁 Project Structure
- notebook.ipynb # Full analysis and modeling pipeline
- dataset.csv # Raw dataset
- README.md # Project documentation
- .gitignore # Ignored system and model files

## 🧰 Libraries Used

- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- xgboost  
- catboost  

---

## 🚀 How to Run

1. Clone the repository:
2. Open the notebook in Google Colab(best) or Jupyter:
3. Ensure dependencies are installed:
4. Run all cells from top to bottom.

---

## 👤 Authors
Fraser Morrow (fmorrow@uwo.ca)

Aidan Tam (atam243@uwo.ca)

Nolan Carvalho (ncarval4@uwo.ca)

Henry Savill (hsavill@uwo.ca)

---

## ✅ License
This project is for academic and educational use.
