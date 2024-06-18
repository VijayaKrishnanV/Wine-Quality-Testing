# Wine-Quality-Testing

This project focuses on predicting wine quality using machine learning models. The dataset includes various chemical properties of wines, such as acidity, pH levels, and alcohol content, along with their quality ratings. Here's a breakdown of the project steps:

Data Exploration and Cleaning:

The dataset is loaded and inspected for missing values.
Missing values are imputed with mean values.
Correlation matrices and histograms are plotted to understand data distributions and relationships.
Feature Engineering:

Non-essential features are dropped based on correlation analysis.
A binary classification task is created where wines with quality ratings above 5 are considered of "best quality."
Model Building and Evaluation:

Three models (Logistic Regression, XGBoost, and Support Vector Classifier) are trained and evaluated.
Model performance metrics such as ROC AUC scores and confusion matrices are computed.
Visualization:

Heatmaps and bar graphs are used to visualize correlations and model accuracies before and after tuning.
This project provides a practical demonstration of using machine learning techniques to assess wine quality based on chemical attributes, aiming to assist in quality control and production decisions in winemaking.

