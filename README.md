# Wine-Quality-Testing

This Python script demonstrates a comprehensive data analysis and machine learning pipeline for a wine quality dataset. The script includes data loading, preprocessing, exploratory data analysis (EDA), model training, and evaluation. It employs various machine learning algorithms to classify wine quality and utilizes performance metrics to assess model effectiveness. The workflow covers handling missing values, normalizing data, feature selection, model training, and generating confusion matrices for evaluation.

Library Imports:

-Essential libraries are imported for data manipulation (pandas, numpy), visualization (matplotlib, seaborn), and machine learning (sklearn, xgboost).


Data Loading:

-The script uploads a CSV file containing wine quality data and loads it into a DataFrame. It then prints the first few rows of the DataFrame, its information, and descriptive statistics.


Data Cleaning:

-Missing values in the dataset are handled by replacing them with the mean of the respective columns.


Exploratory Data Analysis (EDA):

-Histograms are plotted to visualize the distribution of numerical features.
-A bar plot visualizes the relationship between wine quality and alcohol content.
-A heatmap of the correlation matrix is used to identify significant correlations between numerical features.


Feature Engineering:

-The script drops the 'free sulfur dioxide' column if it exists.
-A new binary target column 'best quality' is created based on whether the quality score is greater than 5.
-Categorical values in the 'color' column are replaced with binary values (1 for white and 0 for red).


Feature and Target Assignment:

-The features and target variables are separated. The 'quality' and 'best quality' columns are dropped from the features set.


Data Splitting:

-The dataset is split into training and testing sets using an 80-20 split.


Normalization:

-Data normalization is performed using MinMaxScaler to scale the features to a range of [0, 1].


Model Training and Evaluation:

-Three models are trained: Logistic Regression, XGBoost Classifier, and Support Vector Classifier (SVC).
-Each model's training and validation accuracy are evaluated using the ROC AUC score.
-A confusion matrix is generated and displayed for the XGBoost Classifier.
-A heatmap of feature correlations is plotted.
-A classification report is printed to show detailed performance metrics.
