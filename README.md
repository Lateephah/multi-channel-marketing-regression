# Multi-Channel Marketing Analysis Using Multiple Linear Regression

## Project Overview

This project investigates how multiple marketing channels collectively influence sales performance using Multiple Linear Regression (MLR).

Unlike Simple Linear Regression, which evaluates the impact of a single predictor, this analysis considers the simultaneous effects of different advertising channels and influencer categories to provide more realistic, data-driven recommendations for marketing budget allocation.

The project applies Ordinary Least Squares (OLS) regression using Python and Statsmodels while validating key regression assumptions and assessing multicollinearity among predictors.

---

## Business Problem

Marketing managers often distribute budgets across several channels simultaneously. However, understanding the unique contribution of each channel while accounting for the presence of others remains a challenge.

This project addresses the following question:

> Which marketing channels contribute significantly to Sales after controlling for the effects of other channels, and how should organizations prioritize their marketing investments?

---

## Dataset Description

The dataset contains **572 marketing campaign observations** and the following variables:

| Variable     | Description                                          |
| ------------ | ---------------------------------------------------- |
| TV           | TV advertising expenditure level (Low, Medium, High) |
| Radio        | Radio advertising expenditure                        |
| Social Media | Social Media advertising expenditure                 |
| Influencer   | Influencer category used in the campaign             |
| Sales        | Sales generated from the campaign                    |

No missing values or duplicate observations were identified in the dataset.

---

## Project Objectives

The objectives of this analysis were to:

* Explore and understand the marketing dataset.
* Assess multicollinearity among predictors using correlation matrices and Variance Inflation Factor (VIF).
* Develop a Multiple Linear Regression model using OLS.
* Evaluate model performance using Adjusted R-squared and predictor significance.
* Validate regression assumptions through diagnostic plots.
* Interpret regression coefficients in a business context.
* Provide evidence-based recommendations for marketing budget allocation.

---

## Methodology

### 1. Exploratory Data Analysis

* Examined dataset structure and descriptive statistics.
* Assessed variable distributions and campaign characteristics.

### 2. Data Preprocessing

* Converted categorical variables (TV and Influencer) into dummy variables using one-hot encoding.
* Selected appropriate reference categories to avoid the dummy variable trap.

### 3. Multicollinearity Assessment

* Evaluated pairwise relationships among predictors using correlation matrices.
* Calculated Variance Inflation Factor (VIF) values to detect multicollinearity issues.

### 4. Multiple Linear Regression Modeling

* Split the dataset into training and testing subsets.
* Built an Ordinary Least Squares (OLS) regression model using Statsmodels.
* Compared predictor significance using p-values.

### 5. Diagnostic Evaluation

Regression assumptions were assessed using:

* Residuals vs Fitted Plot (Linearity)
* Residual Distribution Plot (Normality)
* Scale-Location Plot (Homoscedasticity)

---

## Key Findings

The analysis identified which predictors remained statistically significant after controlling for other marketing channels.

Adjusted R-squared was used as the primary measure of model performance because it accounts for the number of predictors included in the model and discourages unnecessary complexity.

Predictors with non-significant effects were evaluated for potential exclusion, balancing interpretability and predictive performance.

---

## Business Insight

Multiple Linear Regression enables marketers to isolate the effect of each advertising channel while holding other factors constant.

For example:

> Holding all other predictors constant, a one-unit increase in a statistically significant marketing channel is associated with an estimated change in Sales equal to its regression coefficient.

This provides a more realistic understanding of marketing effectiveness compared with evaluating channels independently.

---

## Recommendation

Marketing budget decisions should prioritize channels that demonstrate statistically significant positive effects on Sales while maintaining a parsimonious model supported by Adjusted R-squared.

Organizations should avoid allocating resources solely based on intuition and instead rely on evidence derived from multivariate analysis that accounts for interactions among marketing activities.

---

## Author

**Latifah Bashir**

Completed as part of the **3MTT Data Science Program** to demonstrate the practical application of Multiple Linear Regression for multi-channel marketing analysis and evidence-based business decision-making.
