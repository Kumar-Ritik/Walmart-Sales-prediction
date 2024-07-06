# Walmart-Sales-prediction
# Sales Advanced Analysis and Prediction

## Project Overview
This project aims to perform advanced analysis and prediction of weekly sales for a set of stores. The target feature for the prediction is `Weekly_Sales`. Various machine learning models and techniques are employed to ensure accurate prediction and insightful analysis.

## Dataset Features
- **Store**: Store identifier
- **Dept**: Department identifier
- **Date**: Week date
- **Weekly_Sales**: Weekly sales amount (Target variable)
- **IsHoliday**: Boolean flag for holiday week
- **Temperature**: Temperature in the region
- **Fuel_Price**: Fuel price in the region
- **MarkDown1-5**: Data related to promotional markdowns
- **CPI**: Consumer Price Index
- **Unemployment**: Unemployment rate
- **Type**: Type of store
- **Size**: Size of the store

## Data Preprocessing
1. **Handle Missing Values**: MarkDown features with 58% null values are excluded to maintain analysis quality.
2. **Remove Outliers**: Outliers in `Weekly_Sales` were removed as they cannot be negative.
3. **Date Parsing**: Extracted year, month, and week from the `Date` feature.

## Exploratory Data Analysis (EDA)
- Analyzed sales by store type.
- Correlation heatmap for understanding relationships between features.
- Plotted yearly trends of fuel prices and sales.
- Examined relationships between sales and other features like store size and unemployment rate.

## Feature Engineering
- Label encoded categorical features: `IsHoliday` and `Type`.
- Dropped less relevant features like `Date`.

## Feature Importance
Used various techniques to determine feature importance:
- Permutation importance
- Random Forest Regressor
- SHAP (SHapley Additive exPlanations) values

## Model Building and Evaluation
- **Random Forest Regressor**: Applied and visualized feature importance.
- **Decision Tree Regressor**: Evaluated using R2, MSE, and RMSE metrics.
- **XGBoost Regressor**: Achieved high performance with R2 score of 0.944.
- **Ridge Regression**: Applied regularization to improve model generalization.

## Results
- **Random Forest Regressor**:
  - R2 Score: 0.379
  - MSE: 62,845,166.71
  - RMSE: 7,927.49
- **Decision Tree Regressor**:
  - R2 Score: 0.380
  - MSE: 323,184,793.83
  - RMSE: 17,977.34
- **XGBoost Regressor**:
  - R2 Score: 0.944
  - MSE: 28,941,055.96
  - RMSE: 5,379.69
- **Ridge Regression**:
  - R2 Score: 0.944
  - MSE: 28,941,055.96
  - RMSE: 5,379.69

## Installation
To run this project, you need to have Python installed along with the following libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap
## Conclusion
This project successfully segments customer data, analyzes sales trends, and predicts future sales using advanced machine learning techniques. The XGBoost model provided the best performance with a high R2 score and low error metrics.

## Future Work
Incorporate the MarkDown features with advanced imputation techniques.
Explore other machine learning models and hyperparameter tuning.
Deploy the best model as a web service for real-time sales prediction.

## Acknowledgements
Thanks to the kaggle for supplying the dataset.
Gratitude to the open-source community for providing the tools and libraries used in this project.

## Contact
For any inquiries, please contact ara.kumarritik@gmail.com.
