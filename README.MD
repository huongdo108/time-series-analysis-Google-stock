# Overview
This repository performs time series analysis with Google stock's close price. 

# Data 
The data is fetched from YahooFinance. yfinance package needs to be installed in order to fetch data.

# Analysis 
The analysis includes the following parts:

Data Exploratory Analysis

1. Data Exploratory Analysis

    - 1.1 Descriptive Analysis
    - 1.2 Check Stationarity
        - 1.2.1  Decomposition method
        - 1.2.2  Plotting Rolling Statistics
        - 1.2.3  Statistical test
    - 1.3 Stationalize time series
        - 1.3.1  Eliminate trend by smoothing technique
        - 1.3.2  Eliminating Trend and Seasonality by differencing
        - 1.3.3  Eliminating Trend and Seasonality by decomposing
    - 1.4  Autocorrelation Function(ACF) and Partial Autocorrelation Function(PACF)
    
    
2. Prediction models

    - 2.1 Statistical models
        - 2.1.1 ARIMA model
        - 2.1.2  autoSARIMA model
        - 2.1.3  Generalized Autoregressive conditional heteroscedasticity GARCH model
    - 2.2  Neural Network Models
        - 2.2.1  Single step models
            - 2.2.1.1  Feedforward linear model
            - 2.2.1.2  Convolutional Neural Network
            - 2.2.1.3  Recurrent neural network
        - 2.2.2  Multi-step models
            - 2.2.2.1  Single-shot model
            - 2.2.2.2  Autoregressive model with RNN
        - 2.2.3  Model performance comparison

# Result interpretation
Statistical models ARIMA, SARIMA, and GARCH while predict very well the in-sample data, they do to forecast very well the out-of-sample data. Most of the predictions for out-of-sample data, however, lie within 95% of confidence interval.

**ARMA**
<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/ARIMA.PNG" align="centre">

**SARIMA**
<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/SARIMA.PNG" align="centre">

Neural Network models outperform statistical models in prediting out-of-sample data. 

**Single-step model - Feedforward linear model**
<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/linear_result.PNG" align="centre">

**Single-step model - Convolutional Neural Network**
<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/convolutional_result.PNG" align="centre">

**Single-step model - Recurrent neural network**
<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/rnn_result.PNG" align="centre">

Single-step models outperform multi-step models. Linear model supprisingly outperforms Convolutionary and LSTM since LSTM is supposed to be able to learn dependecies better. LSTM with a better architecture might outperform linear model.

<img src="https://github.com/huongdo108/time-series-analysis-Google-stock/blob/master/images/neural_results.PNG" align="centre">

# How to run
Install packages and dependencies in requirements.txt
Run the google_stock_analysis.ipynb