# 🏠 Housing Price Prediction

This project predicts housing prices in Tehran using various Machine Learning regression models.

---

🏗️ Final Integration: HousingForecast Meta-Model
At the end of the project, I developed a final stacked model called HousingForecast.
It combines three base models — Random Forest, ElasticNet, and XGBoost — using a Linear Regression meta-learner.

📊 Results:

Mean Absolute Error (MAE): ~1,000,000,000 IRR

R² Score: 0.8432

After applying Isolation Forest and removing ~10% of the most extreme outliers:

MAE improved to ~575,000,000 IRR

The prediction range became more realistic

🚧 Limitations faced:

Small dataset (~300 samples)

Highly skewed target values (from 66 million to 66 billion IRR)

Missing critical features such as:

Building age

Floor level

Renovation history

Accurate geographic coordinates (only average neighborhood price was used)

📌 Conclusion:
Despite the limitations, the stacking approach showed a meaningful performance boost. The results highlight how much cleaner data and richer features can improve regression models in real estate prediction tasks.

If I get access to more detailed property data in the future, I plan to revisit this project and push the model performance further.



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



- The current models have high MAE (~1 billion IRR) across all approaches tested (Linear, Polynomial, Ridge, Lasso, Random Forest, ElasticNet).
- The main reason is the lack of rich and clean data. For example:
  - No features like building age, floor level, or renovation status.
  - Location is very general (only neighborhood average).
  - Possible outliers that impact the target price.
- With more detailed data and proper feature engineering, the accuracy can significantly improve.

---
**Outlier Removal:**  
By removing ~10% of samples detected as outliers using Isolation Forest, the MAE dropped significantly from ~1 billion IRR to ~575 million IRR in Gradient Boosting Regression.  
This shows that proper data cleaning and outlier handling can greatly improve model performance.
## 🚫 Limitations

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
