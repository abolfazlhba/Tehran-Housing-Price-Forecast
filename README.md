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



## 🚫 Limitations

- The current models have high MAE (~1 billion IRR) across all approaches tested (Linear, Polynomial, Ridge, Lasso, Random Forest, ElasticNet).
- The main reason is the lack of rich and clean data. For example:
  - No features like building age, floor level, or renovation status.
  - Location is very general (only neighborhood average).
  - Possible outliers that impact the target price.
- With more detailed data and proper feature engineering, the accuracy can significantly improve.

---

## 🔭 Next Steps

- Collect more detailed features.
- Try advanced models (Gradient Boosting, XGBoost).
- Perform more robust outlier detection.
- Tune hyperparameters with GridSearch or RandomizedSearch.

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
