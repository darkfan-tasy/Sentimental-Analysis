# Project Report: Stock Price Prediction with ARIMA and LSTM

## Introduction

This project aims to predict the stock prices of the SENSEX (S&P BSE SENSEX) using a hybrid model that combines numerical analysis of historical stock prices with sentiment analysis of news headlines. The hybrid model includes ARIMA for time series forecasting and LSTM for deep learning-based predictions.

## Table of Contents

1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Methodology](#methodology)
   - [ARIMA Model](#arima-model)
   - [LSTM Model](#lstm-model)
4. [Results](#results)
5. [Conclusion](#conclusion)
6. [Future Work](#future-work)
7. [References](#references)

## Data Description

The dataset consists of historical stock prices of SENSEX and news headlines. 

### Data Preprocessing

- **Stock Prices**: The historical stock prices data is cleaned and prepared for the ARIMA and LSTM models.
- **News Headlines**: Sentiment analysis is performed on the headlines to derive sentiment scores, which are then integrated with the stock price data.

## Methodology

### ARIMA Model

The ARIMA (AutoRegressive Integrated Moving Average) model is used for time series forecasting. The steps include:

1. **Data Preprocessing**: Handling missing values and differencing to make the time series stationary.
2. **Model Selection**: Using ACF and PACF plots to select appropriate p, d, q parameters.
3. **Model Training**: Fitting the ARIMA model to the training data.
4. **Forecasting**: Making predictions on the test data.
5. **Evaluation**: Calculating Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) to evaluate model performance.

### LSTM Model

The LSTM (Long Short-Term Memory) model is a type of recurrent neural network (RNN) well-suited for sequence prediction problems. The steps include:

1. **Data Scaling**: Normalizing the data using MinMaxScaler.
2. **Data Preparation**: Creating sequences of stock prices for the LSTM model.
3. **Model Architecture**: Building an LSTM model with multiple layers.
4. **Model Training**: Training the model on the training data.
5. **Evaluation**: Calculating MAE and RMSE to evaluate model performance.
6. **Visualization**: Plotting the predicted prices against actual prices.

## Results

### ARIMA Model

- **Training Results**: The ARIMA model was trained on historical stock price data.
- **Evaluation Metrics**: 
  - MAE: 169.63000293456045
  - RMSE: 280.8538601203419

### LSTM Model

- **Training Results**: The LSTM model was trained on scaled stock price data.
- **Evaluation Metrics**:
  - MAE: 632.8832125453321
  - RMSE: 841.1447847292411

### Improved LSTM Model

- **Training Results**: The improved LSTM model was trained with additional dropout layers to prevent overfitting.
- **Evaluation Metrics**:
  - Improved LSTM Model MAE: 540.2297851851448
  - Improved LSTM Model RMSE: 743.7666062668358

## Conclusion

The hybrid model combining ARIMA and LSTM provides a robust approach to stock price prediction. While ARIMA is effective for capturing linear patterns in time series data, LSTM excels at capturing non-linear patterns and sequential dependencies.

## Future Work

- Integrate more advanced sentiment analysis techniques for better feature extraction from news headlines.
- Explore other deep learning models like GRU and Transformer for stock price prediction.
- Incorporate additional features such as macroeconomic indicators for improved prediction accuracy.
