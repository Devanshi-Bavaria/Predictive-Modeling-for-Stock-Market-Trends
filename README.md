# Predictive Modeling for Stock Market Trends

## Overview

This repository encompasses a detailed analysis of stock price data, offering insights into various aspects, including data preprocessing, exploratory data analysis (EDA), clustering, correlation analysis, and the construction of a predictive model. The analysis is conducted on a substantial financial dataset, covering both descriptive and predictive dimensions.

## Table of Contents

1. [Data Preprocessing and Exploratory Data Analysis (EDA)](#data-preprocessing-and-eda)
2. [Clustering Analysis](#clustering-analysis)
3. [Correlation Analysis](#correlation-analysis)
4. [Stock Closing Trajectory](#stock-closing-trajectory)
5. [Permutation Test](#permutation-test)
6. [Prediction Model](#prediction-model)

## Data Preprocessing and Exploratory Data Analysis (EDA) <a name="data-preprocessing-and-eda"></a>

The analysis initiates with an exhaustive data preprocessing phase and explores the dataset's nuances. Key steps in this phase include:

- **Imputation:** Addressing missing values, specifically in the 'far_price' and 'near_price' columns. Imputation is strategically performed based on empirical observations, resulting in an effective imputation strategy.
- **Scaling:** Applying Min-Max scaling to standardize selected features. This ensures uniformity in variable scales, a crucial factor for machine learning model stability.
- **Feature Engineering:** Creating meaningful features such as 'bid_ask_spread_percentage' and 'reference_price_wap_ratio.' These features offer valuable insights into market dynamics.

## Clustering Analysis <a name="clustering-analysis"></a>

A clustering analysis is conducted using the K-means algorithm to identify groups of stocks with similar characteristics. Key components of this analysis include:

- **Optimal Cluster Number Determination:** Employing the Elbow method to identify the optimal number of clusters that best represent the underlying structure in the data.
- **Visual Representation:** Utilizing a t-SNE plot to visually represent the clustering results, aiding in the interpretation of stock relationships.

## Correlation Analysis <a name="correlation-analysis"></a>

This section delves into the correlation of stock closing trajectories to discern whether they exhibit a high correlation, indicating market trends, or are essentially random. The analysis encompasses:

- **Daily Correlation Calculation:** Computing and visualizing daily correlations between stock closing trajectories.
- **Statistical Tests:** Employing statistical tests such as the one-sample t-test and Q-Q plot to evaluate the significance of correlations.
- **Hierarchical Clustering:** Using hierarchical clustering to explore the grouping of related stocks based on their closing trajectories.

## Stock Closing Trajectory <a name="stock-closing-trajectory"></a>

This section scrutinizes the closing trajectory of stocks on each day, aiming to determine whether it is highly correlated, indicative of market trends, or essentially random. The analysis involves:

- **Daily Performance Categorization:** Categorizing stock performance as 'up,' 'down,' or 'no change' based on daily closing trajectory.
- **Heatmap Visualization:** Creating a heatmap to visualize daily correlations between stocks' closing trajectories.
- **Dendrogram Construction:** Employing hierarchical clustering to further explore the clustering of related stocks.

## Permutation Test <a name="permutation-test"></a>

A permutation test is conducted to assess the statistical confidence in the conclusion regarding the randomness of stock closing trajectories. Key steps include:

- **Test Statistic Calculation:** Defining a test statistic (mean) for the original data and calculating the same for permuted datasets.
- **P-Value Determination:** Calculating the p-value by comparing the original statistic to permuted statistics.
- **Conclusion Drawing:** Making conclusions based on the p-value and significance level.

## Prediction Model <a name="prediction-model"></a>

The analysis concludes with the construction of a predictive model for stock prices. Four regression models—Linear Regression, Ridge Regression, Lasso Regression, and HistGradientBoosting—are evaluated using 5-fold cross-validation. The chosen model, HistGradientBoostingRegressor, is highlighted for its superior performance in predicting the target variable.
