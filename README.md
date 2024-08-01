# Wine Quality Prediction Project

## Project Overview

This project aims to classify wine quality based on various chemical properties using different machine learning models. The models implemented include Logistic Regression, XGBoost, and Support Vector Classifier (SVC). The dataset used is the Wine Quality Dataset, which contains both red and white wine samples with various chemical properties and their corresponding quality ratings.

## Dataset

The dataset used in this project is `winequalityN.csv`. The dataset includes the following columns:

- `type`: The type of wine (red or white)
- `fixed acidity`
- `volatile acidity`
- `citric acid`
- `residual sugar`
- `chlorides`
- `free sulfur dioxide`
- `total sulfur dioxide`
- `density`
- `pH`
- `sulphates`
- `alcohol`
- `quality`: Quality rating of the wine

## Project Structure

```
Wine-Quality-Prediction/
├── winequalityN.csv
├── model_training.ipynb
├── README.md
```

- `winequalityN.csv`: The dataset file.
- `model_training.ipynb`: Jupyter notebook for data analysis, model training, and evaluation.
- `README.md`: This file.


## Running the Code

### 1. Open Jupyter Notebook

To start the Jupyter notebook, run the following command in your terminal:

```bash
jupyter notebook
```

This will open the Jupyter notebook interface in your web browser. Navigate to the `model_training.ipynb` file and open it.

### 2. Run the Notebook

Follow the instructions in the notebook to:
1. **Load the Dataset**: Load the `winequalityN.csv` file.
2. **Data Preprocessing**: Handle missing values and encode categorical variables.
3. **Data Visualization**: Plot histograms and heatmaps to understand data distribution and correlations.
4. **Feature Engineering**: Create new features if necessary.
5. **Model Training**: Train Logistic Regression, XGBoost, and SVC models.
6. **Model Evaluation**: Evaluate the models using ROC-AUC score, confusion matrix, and classification report.

## Results

### Data Preprocessing

- Missing values were filled with the mean of the respective columns.
- The `type` column was encoded (white = 1, red = 0).
- A new target column `best quality` was created where wines with a quality score > 5 were labeled as 1 (good quality) and others as 0 (bad quality).

### Model Performance

Three models were trained and evaluated:

1. **Logistic Regression**
   - Training Accuracy: 0.698
   - Validation Accuracy: 0.701

2. **XGBoost**
   - Training Accuracy: 0.978
   - Validation Accuracy: 0.788

3. **Support Vector Classifier (SVC)**
   - Training Accuracy: 0.714
   - Validation Accuracy: 0.711

### Confusion Matrix for XGBoost

```python
cm = confusion_matrix(ytest, models[1].predict(xtest))
disp = ConfusionMatrixDisplay(confusion_matrix=cm)
disp.plot()
plt.show()
```

### Classification Report for XGBoost

```python
print(metrics.classification_report(ytest, models[1].predict(xtest)))
```

```
              precision    recall  f1-score   support

           0       0.77      0.70      0.73       474
           1       0.83      0.88      0.86       826

    accuracy                           0.81      1300
   macro avg       0.80      0.79      0.79      1300
weighted avg       0.81      0.81      0.81      1300
```
