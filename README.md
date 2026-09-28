# 🏠 King County House Price Prediction

## Overview

This project explores house price prediction in **King County, Washington**, using residential property sales data from the Seattle area.

The objective is to estimate house prices from property characteristics such as living area, bedrooms, bathrooms, grade, location, construction year, and other housing features.

A **Linear Regression** model is used as a baseline regression approach.

---

## Dataset

The dataset contains residential property sales from King County between **2014 and 2015**.

Selected features include:

- Bedrooms and bathrooms
- Living and lot area
- Floors
- Waterfront and view
- Condition and grade
- Construction and renovation year
- ZIP code
- Latitude and longitude
- Neighboring property information
- House price

Target variable:

**`price`**

---

## Approach

The project follows the following workflow:

1. Exploratory Data Analysis
2. Missing value inspection
3. Correlation analysis
4. Feature preparation
5. House age calculation
6. Outlier removal
7. Feature transformation
8. Categorical encoding
9. Train-test split
10. Linear Regression modeling
11. Model evaluation
12. Prediction and residual visualization

---

## Feature Engineering

Several preprocessing steps were applied before modeling:

- Removed the `id` column
- Calculated house age using sale year and construction year
- Removed selected extreme values using the 97th percentile
- Converted ZIP code into a categorical feature
- Converted renovation and basement information into binary variables
- Converted categorical variables using dummy encoding

---

## Model

The target variable is continuous, therefore a **Linear Regression** model was used.

The dataset was divided into:

- **80% Training Data**
- **20% Test Data**

---

## Results

| Metric | Result |
| --- | ---: |
| R² Score | **0.4475** |
| RMSE | **158,321.39** |
| MAE | **124,644.85** |

The model explains approximately **45% of the variation in house prices**.

The results suggest that a linear model captures part of the relationship between housing characteristics and price, while more complex relationships remain unexplained.

---

## Visualizations

The notebook includes:

- Correlation heatmap
- House price distribution
- Bedroom distribution
- Property view distribution
- Actual vs Predicted Prices
- Residual distribution

---

## Technologies

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn` `Jupyter Notebook`

---

## Conclusion

This project presents a complete regression workflow for house price prediction.

Linear Regression provides a useful baseline, while the evaluation results indicate that future improvements could include additional feature engineering or more flexible regression models.
