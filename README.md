# AI-Driven Ad Budget Allocation

An AI-powered solution designed to automate and optimize advertisement budget allocation across multiple digital platforms like Google Ads, Meta Ads, and Microsoft Ads. By leveraging machine learning and historical performance data, this solution helps businesses make data-driven decisions to maximize return on investment (ROI) and achieve marketing goals.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Approach and Methodology](#approach-and-methodology)
  - [1. Data Preprocessing](#1-data-preprocessing)
  - [2. Model Selection and Evaluation](#2-model-selection-and-evaluation)
  - [3. Budget Allocation Algorithm](#3-budget-allocation-algorithm)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Results and Insights](#results-and-insights)
- [Conclusion](#conclusion)


## Introduction

Digital advertising is a rapidly evolving field, and optimizing ad budget allocation across multiple platforms is crucial for any business aiming to maximize ROI. This project offers an AI-driven approach to dynamically distribute advertising budgets based on key performance indicators (KPIs) such as impressions, clicks, conversions, and revenue.

The system uses historical performance data from platforms like Google Ads, Meta Ads, and Microsoft Ads to make informed decisions, improving both marketing efficiency and profitability.

## Features
- Automated budget allocation across platforms based on machine learning predictions.
- Data preprocessing including handling missing values and feature engineering.
- Comparative analysis of models like Linear Regression, Random Forest, and AutoML.
- Proportional budget distribution to maximize predicted revenue while ensuring minimum platform allocation.
- Insights-driven decision-making for improved ROAS (Return on Advertising Spend).

## Approach and Methodology

### 1. Data Preprocessing
- **Exploratory Data Analysis (EDA):** Key trends such as Meta's cost-effective conversions and Google’s high-revenue but high-cost campaigns were identified.
- **Handling Missing Values:** Numerical nulls were replaced with the median, while categorical nulls were filled with zeros.
- **Z-Score Normalization:** Standardization of features to avoid skewing model learning.
- **Feature Engineering:** Enhanced model performance by combining features, improving the R² score from ~0.85 to 0.94.

### 2. Model Selection and Evaluation
- **Feature Preparation:** Selected key features like impressions, clicks, cost, CTR, CPC, CPCV, CVR, and effective reach rate for predicting revenue.
- **Model Comparison:**
  - **Linear Regression:** RMSE: 0.754, R² Score: 0.503
  - **Random Forest:** RMSE: 0.266, R² Score: 0.938
  - **AutoML (Best Model - LGBMRegressor):** RMSE: 0.247, R² Score: 0.946

### 3. Budget Allocation Algorithm
- **Define Budget Parameters:**
  - Total Budget: Allocate 70% of the budget based on predicted revenue.
  - Minimum Allocation: Ensure each platform gets at least 10% of the budget.
- **Budget Calculation:** Allocate budget proportionally to predicted revenue, with adjustments to meet the minimum budget requirement.
- **Final Summary:** Outputs adjusted budget allocations and predicted revenue by platform.

## Technologies Used
- **Programming Language:** Python
- **Machine Learning:** AutoML, LightGBM, Random Forest, Linear Regression
- **Data Handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn

  ## Results and Insights
- The  ExtraTreesRegressor outperformed other models, striking the right balance between prediction accuracy and error.
- More budget should be allocated to Google Ads as it showed the greatest potential for scaling and generating profits, enhancing overall ROAS.

## Conclusion
This project demonstrates how AI-driven budget allocation can save time and improve decision-making in digital marketing. By automating the allocation process and optimizing for key KPIs, businesses can achieve better marketing efficiency and profitability.

