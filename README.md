# Tesla Stock Price Prediction

This repository contains a machine learning model to predict the stock price trend of Tesla (TSLA) using historical stock data. The project uses various classification models to predict whether the stock price will go up or down based on historical features such as `Open`, `High`, `Low`, `Close`, and `Volume`. The models used include `Logistic Regression`, `Support Vector Classifier (SVC)`, and `XGBoost Classifier`.

## Dataset

The dataset used in this project is Tesla's historical stock price data, which includes the following columns:

- **Date**: The date of the stock data.
- **Open**: The price at which the stock opened for the day.
- **High**: The highest price reached by the stock during the day.
- **Low**: The lowest price reached by the stock during the day.
- **Close**: The price at which the stock closed at the end of the day.
- **Volume**: The number of shares traded during the day.
- **Adj Close**: The adjusted closing price (which accounts for events like stock splits and dividends).

## Requirements

To run the code, make sure you have the following libraries installed:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

You can install these dependencies using the following command:

```bash
pip install -r requirements.txt
```

## Steps to Run the Project

1. **Data Preprocessing:**
   - The data is loaded from a CSV file, and unnecessary columns such as `Adj Close` are dropped.
   - Missing values are checked, and if present, handled accordingly.
   
2. **Exploratory Data Analysis (EDA):**
   - The project uses visualization tools like line plots, histograms, and boxplots to explore the stock price trends.
   
3. **Feature Engineering:**
   - The target variable `target` is created, where:
     - `1` indicates the price will go up the next day.
     - `0` indicates the price will go down the next day.
   - The features used are `Open`, `High`, `Low`, `Close`, and `Volume`.
   
4. **Model Training:**
   - The dataset is split into training and validation sets.
   - Three models are trained:
     - **Logistic Regression**
     - **Support Vector Classifier (SVC)**
     - **XGBoost Classifier**
   
5. **Model Evaluation:**
   - The models are evaluated using the **ROC AUC score** on both the training and validation datasets.
   - Confusion matrix visualizations are created for each model to evaluate its performance.

## Evaluation Results

The models' performance on training and validation data is as follows:

- **Logistic Regression:**
  - Training Accuracy: 0.51
  - Validation Accuracy: 0.53

- **Support Vector Classifier (SVC) with Polynomial Kernel:**
  - Training Accuracy: 0.50
  - Validation Accuracy: 0.50

- **XGBoost Classifier:**
  - Training Accuracy: 0.95
  - Validation Accuracy: 0.60

## Visualizations

The project includes several visualizations to understand the stock price trends:

- Line plots of the `Close` and `Open` stock prices.
- Histograms and boxplots to visualize the distribution of the features.

## Getting Started

To get started, clone the repository to your local machine:

```bash
git clone https://github.com/BhavinDabhi29/stock-market-prediction.git
```

Change into the project directory:

```bash
cd stock-market-prediction
```

Run the Jupyter Notebook or Python script to train the models and see the results:

```bash
python stock price prediction.ipynb
```
