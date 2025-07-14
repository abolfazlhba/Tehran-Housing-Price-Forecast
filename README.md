# 🏠 Housing Price Prediction

This project predicts housing prices in Tehran using various Machine Learning regression models.

---

## 📂 Project Overview

The goal is to predict the house price based on features like:
- `Area` (square meters)
- `Room` (number of rooms)
- `Parking` (parking availability)
- `Warehouse` (storage availability)
- `Elevator` (elevator availability)
- `MeanPriceA` (average price of the neighborhood)

---

## ⚙️ Methods Used

- 📈 **Multiple Linear Regression**
- 📐 **Polynomial Features Regression**
- 🧮 **Lasso Regression (L1)**
- 🧩 **Ridge Regression (L2)**
- 🌲 **Random Forest Regression**
- ⚡ **ElasticNet Regression**
- 🔍 **Cross Validation (RepeatedKFold)**
- ⚖️ **Feature Scaling (StandardScaler)**

---

## 📊 Main Results

| Model | R2 Score | MAE |
|-------|----------|-----|
| Linear Regression | 0.71 | ~1,000,000,000 |
| Polynomial Regression (deg=2) | 0.80 | ~900,000,000 |
| Ridge Regression | 0.77 | ~950,000,000 |
| Lasso Regression | 0.74 | ~980,000,000 |
| Random Forest | 0.85 | ~850,000,000 |

✅ **Residual Plot:**  
![](results/plots/residual_plot.png)

---

## 📁 Project Structure

```bash
.
├── data/
│   ├── HouseInformation.csv
├── Housing Forecast/
│   ├── ElasticNetModel.ipynb
│   ├── LassoRegression.ipynb
│   ├── Multiple Regression Model.ipynb
│   ├── Polynomial Features Model.ipynb
│   ├── RandomForestRegression.ipynb
│   ├── Ridge And Polynomial Features Model.ipynb
│   ├── Ridge Regression Model.ipynb
│   ├── GradientBoostingRegressor.ipynb
├── Models/
│   ├── ElasticNetModel
│   ├── ElasticNetModelWithPolynomialFeaturesModel
│   ├── LassoRegression.pkl
│   ├── LassoRegressionWithPolynomialFeaturesModel.pkl
│   ├── LinearRegCleanedModel.pkl
│   ├── LinearRegMiniCleanModel.pkl
│   ├── LinearRegRawDataModel.pkl
│   ├── PolynomialFeatureDgree2Model.pkl
│   ├── PolynomialFeatureDgree2RawDataModel.pkl
│   ├── PolynomialFeatureDgree3Model.pkl
│   ├── PolynomialFeatureDgree4Model.pkl
│   ├── Ridge&PolyRegressionModel.pkl
│   ├── RidgeRegressionModel.pkl
├── requirements.txt
├── README.md
