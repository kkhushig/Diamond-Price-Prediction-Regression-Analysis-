# Diamond Price Prediction - Regression Analysis

This project aims to analyze the diamonds dataset to predict diamond prices based on various characteristics using regression analysis. The dataset contains approximately 54,000 entries, each with features like carat, cut, color, clarity, depth, table, and dimensions. Several regression models are implemented and compared to identify the most effective predictor.

## Table of Contents
- [Introduction](#introduction)
- [Literature Review](#literature-review)
- [Data Description](#data-description)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Regression Analysis](#regression-analysis)
- [Results](#results)
- [Conclusion](#conclusion)
- [Installation](#installation)

## Introduction
The chosen dataset for this project is `diamonds.csv`, which includes a variety of attributes related to diamonds. The goal is to uncover patterns and relationships between these attributes and diamond pricing, enhancing our understanding of the diamond market. The analysis will employ seven regression models, including:
- Simple Linear Regression
- Multiple Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- L1 (Lasso) Regression
- L2 (Ridge) Regression
- MLP (Multi-Layer Perceptron) Regressor

## Literature Review
Regression analysis serves as a powerful statistical method to explore relationships between variables, applicable across various disciplines. Key steps in data preparation include data cleaning, transformation, and integration to ensure robust analysis. This project emphasizes the importance of these preprocessing steps for accurate and meaningful outcomes.

## Data Description
The dataset contains 53,940 entries and 10 features related to diamonds, including:

| Feature | Description |
| ------- | ----------- |
| `carat` | Weight of the diamond |
| `cut` | Quality of the cut (e.g., Ideal, Premium, Good) |
| `color` | Diamond color, ranging from D (best) to J (worst) |
| `clarity` | Clarity rating (e.g., SI2, SI1, VS1, VS2) |
| `depth` | Total depth percentage |
| `table` | Width of the diamond's top relative to its widest point |
| `x` | Length of the diamond (mm) |
| `y` | Width of the diamond (mm) |
| `z` | Depth of the diamond (mm) |
| **Target Variable** | `price`: Price of the diamond |

## Data Preprocessing
Data preprocessing is crucial for ensuring that the dataset is clean and ready for analysis. Steps include:

1. **Checking for Missing Values**: No missing values were found in any columns.
2. **Label Encoding**: Converts categorical variables (`cut`, `color`, `clarity`) into numeric form.
3. **Handling Duplicates**: Duplicate rows were removed.
4. **Removing Outliers**: Extreme values were identified and removed using the Interquartile Range (IQR) method.

## Exploratory Data Analysis (EDA)
EDA was performed to summarize the main characteristics of the dataset, including:
- Numerical and categorical summaries
- Histograms and boxplots to visualize data distribution and identify trends
- Correlation matrices to uncover relationships between variables

## Regression Analysis
### Feature Selection Methods
Different methods, including correlation analysis and ANOVA, were utilized to select significant features influencing diamond prices.

### Regression Models
1. **Simple Linear Regression**
2. **Multiple Linear Regression**
3. **Decision Tree Regressor**
4. **Random Forest Regressor**
5. **L1 Regularization (Lasso)**
6. **L2 Regularization (Ridge)**
7. **Multi-Layer Perceptron (MLP) Regressor**

### Model Performance
Each model's performance was evaluated based on R² (Coefficient of Determination) and MSE (Mean Squared Error). A detailed comparison of the models' performances is provided in the Results section.

## Results
The models demonstrated robust performance, with negligible differences between training and testing R² values. The Multi-Layer Perceptron (MLP) regressor yielded the highest predictive accuracy.

| Method                              | Train R² | Test R² | Difference |
|-------------------------------------|----------|---------|------------|
| Multi-Layer Perceptron Regressor   | 0.984    | 0.982   | 0.002      |
| Random Forest Regressor             | 0.9521   | 0.9446  | 0.0075     |
| Decision Tree Regressor             | 0.9466   | 0.9423  | 0.0043     |
| Multiple Linear (Polynomial) Regression | 0.944  | 0.930   | 0.014      |
| Simple Linear Regression             | 0.892    | 0.889   | 0.003      |
| Lasso Regression (L1)               | 0.8918   | 0.8886  | 0.0032     |
| Ridge Regression (L2)               | 0.8918   | 0.8885  | 0.0033     |


## Conclusion
Comprehensive data preprocessing contributed to the models' predictive power, ensuring reliable and generalizable results. The MLP regressor emerged as the most effective model for diamond price prediction.

## Installation
To run this project, you need to have Python installed. The required libraries can be installed using pip:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
