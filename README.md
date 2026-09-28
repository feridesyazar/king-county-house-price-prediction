# 🏠 King County House Price Prediction

## Project Overview

This project predicts house prices in **King County, Washington**, including Seattle, using housing data from homes sold between May 2014 and May 2015.

A **Linear Regression** model is used to estimate house prices based on property characteristics such as bedrooms, bathrooms, living area, condition, grade, location, and construction year.

The workflow includes exploratory data analysis, data preparation, feature engineering, train-test splitting, regression modeling, evaluation, and visualization of prediction results.

---

## Dataset

The dataset contains residential property sales data from King County, Washington.

Main features include:

- Bedrooms
- Bathrooms
- Living area
- Lot area
- Floors
- Waterfront
- View
- Condition
- Grade
- Construction year
- Renovation information
- ZIP code
- Latitude and longitude
- Neighboring property information
- House price

The dataset file is included in this repository.

---

## Project Workflow

1. Load and inspect the dataset
2. Check data types and missing values
3. Analyze correlations between numerical variables
4. Remove the identifier column
5. Create house age from sale year and construction year
6. Remove selected extreme values
7. Transform selected numerical features
8. Convert categorical variables into dummy variables
9. Split the data into training and test sets
10. Train a Linear Regression model
11. Evaluate the model using R², RMSE, and MAE
12. Visualize actual vs predicted prices and residuals

---

## Data Preparation

The `id` column is removed because it does not provide useful information for house price prediction.

A new `age` feature is calculated using the sale year and construction year.

Selected extreme values are removed using the 97th percentile as a simple threshold.

ZIP code is treated as a categorical feature, while renovation and basement information are converted into binary variables.

---

## Modeling

A **Linear Regression** model is used because the target variable, house price, is continuous.

The dataset is divided into training and test sets using an 80/20 split.

---

## Model Evaluation

The final model achieved:

| Metric | Result |
| --- | ---: |
| R² Score | **0.4475** |
| RMSE | **158,321.39** |
| MAE | **124,644.85** |

The model explains approximately **45% of the variation in house prices**.

The remaining prediction error suggests that house prices depend on more complex relationships that are not fully captured by a linear regression model.

---

## Visualizations

The project includes:

- Correlation heatmap
- House price distribution
- Bedroom distribution
- Property view distribution
- Actual vs predicted house prices
- Residual distribution

---

## Technologies

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Conclusion

This project applies **Linear Regression** to predict house prices in King County, Washington.

The workflow includes exploratory data analysis, outlier removal, feature transformation, categorical encoding, train-test splitting, regression modeling, and model evaluation.

The final model achieved an **R² Score of 0.4475**, with an **RMSE of 158,321.39** and an **MAE of 124,644.85**.

The results provide a baseline for house price prediction and show that additional modeling approaches may be needed to capture more complex relationships in the housing data.



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
