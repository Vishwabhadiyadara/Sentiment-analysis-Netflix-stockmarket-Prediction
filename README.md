# Sentiment Analysis of Twitter Data for Predicting Netflix Stock Price

## Project Overview

This project investigates the relationship between Twitter sentiment and Netflix's stock price. By employing sentiment analysis and machine learning techniques, we aim to forecast future stock trends based on social media data.

## Problem Setting

In the contemporary landscape of finance and technology, the intersection of social media and stock market analysis presents a compelling domain for exploration. This project focuses on:

- Sentiment Trend Analysis
- Interactive Network Mapping
- Influential Entity Identification
- Sub-Community Detection

## Problem Definition

The goal is to analyze social media data related to Netflix Inc and forecast its future stock trends using sentiment classification. This project explores the potential correlations between public sentiment and market dynamics.

## Data Sources

- **Twitter Data:** Extracted from the "Netflix Stock Dataset with Twitter Sentiment" available on Kaggle.
- **Stock Data:** Historical prices for Netflix stocks obtained from Yahoo Finance, spanning from January 1, 2018, to July 7, 2022.

## Data Description

- **Financial Data:** Includes opening price, closing price, high, low, and adjusted closing price of Netflix stock.
- **Twitter Data:** Contains sentiment scores (positive, neutral, negative) derived from tweets mentioning Netflix.

## Data Exploration

Visualization methods include:

- **Time-Series Analysis:** Tracking changes in Twitter sentiment and Netflix stock prices over time.

## Data Mining Tasks

Key tasks include:

- **Data Cleaning:** Removing URLs, hashtags, numerical values, and translating emojis into text.
- **Sentiment Analysis:** Using the “twitter-slm-roberta-base-sentiment" pre-trained model.
- **Data Transformation and Integration:** Normalizing polarity scores and integrating them with stock price data.

## Data Mining Models/Methods

Two main models were employed:

### ARIMA Model Implementation

- **Autoregressive Integrated Moving Average (ARIMA):** Used for univariate time series data modeling.
- **SARIMA:** Seasonal ARIMA, enhancing the model's accuracy in capturing regular fluctuations.

### CNN-LSTM Model Implementation

- **CNN Component:** Acts as a feature extractor, identifying key patterns within the sentiment data.
- **LSTM Component:** Learns dependencies in long sequences of stock price data.

## Performance Evaluation

Evaluation metrics included:

- **Mean Squared Error (MSE):** Used to measure forecasting accuracy.
- **Model Comparison:** Evaluating the impact of sentiment data on forecasting accuracy.

## Project Results

Key findings underscore the nuanced relationship between public sentiment and stock market performance:

- **Enhanced Model Accuracy:** Sentiment analysis improved LSTM model accuracy.
- **Deliverables:** Development of ARIMA and CNN-LSTM models.

## Impact of the Project Outcomes

The project outcomes enhance the accuracy of stock price predictions and provide a framework for integrating sentiment analysis into financial models, offering significant value to investors and financial analysts.

## References

1. Aadhitya, A., et al. "Predicting Stock Market Time-Series Data using CNN-LSTM Neural Network Model." No. 2305.14378. 2023.
2. Winata, Aditya, Sena Kumara, and Derwin Suhartono. "Predicting stock market prices using time series SARIMA." 2021 1st International Conference on Computer Science and Artificial Intelligence (ICCSAI). Vol. 1. IEEE, 2021.
3. Barbieri, Francesco, et al. "TweetEval: Unified benchmark and comparative evaluation for tweet classification." arXiv preprint arXiv:2010.12421 (2020).
