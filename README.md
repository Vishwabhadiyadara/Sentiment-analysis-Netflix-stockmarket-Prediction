# Stock Market Prediction Enhancement through Twitter Sentiment Analysis

## Table of Contents:
- [Introduction](#introduction)
- [Conceptual Framework](#conceptual-framework)
  - [The Role of CNN in Time Series Analysis](#the-role-of-cnn-in-time-series-analysis)
  - [The Application of LSTM in Time Series](#the-application-of-lstm-in-time-series)
  - [Overview of ARIMA](#overview-of-arima)
  - [Extending ARIMA to SARIMA for Seasonal Data](#extending-arima-to-sarima-for-seasonal-data)
- [Project Methodology](#project-methodology)
  - [Project Architecture](#project-architecture)
  - [Data Acquisition](#data-acquisition)
  - [Data Cleaning](#data-cleaning)
  - [Sentiment Analysis Implementation](#sentiment-analysis-implementation)
  - [Data Integration](#data-integration)
    - [Preparing Data for ARIMA](#preparing-data-for-arima)
    - [Preparing Data for CNN-LSTM](#preparing-data-for-cnn-lstm)
  - [Model Development](#model-development)
    - [ARIMA Modeling](#arima-modeling)
    - [CNN-LSTM Model Design](#cnn-lstm-model-design)
- [Experimental Results](#experimental-results)
- [Conclusions](#conclusions)
- [Implementation Guide](#implementation-guide)
  - [How to Scrape Tweets](#how-to-scrape-tweets)
  - [How to Perform Sentiment Analysis](#how-to-perform-sentiment-analysis)
- [References and Further Reading](#references-and-further-reading)
- [Project Contributors](#project-contributors)

## Introduction:
![Introduction Image](https://i.morioh.com/2020/02/04/beef36fd707d.jpg)
This project aims to enhance stock market predictions by integrating sentiment analysis from Twitter, recognizing that social media's influence and other unpredictable factors play significant roles in market movements.

## Conceptual Framework:
### The Role of CNN in Time Series Analysis
Convolutional Neural Networks (CNNs), especially 1D-CNNs, are adept at processing time series data, capturing essential patterns and reducing noise, thereby ideal for analyzing fixed-window time series data.

### The Application of LSTM in Time Series
Long Short-Term Memory (LSTM) networks excel in capturing long-term dependencies within time series data, making them particularly useful for predicting sequences in stock market trends.

### Overview of ARIMA
![ARIMA Image](https://cdn.analyticsvidhya.com/wp-content/uploads/2024/04/arima-model-scaled.jpg)
Autoregressive Integrated Moving Average (ARIMA) is a forecasting model that uses time series data to predict future points. ARIMA models are characterized by their components:
- **Auto-Regressive (AR)**: The model uses the dependent relationship between an observation and a number of lagged observations.
- **Integrated (I)**: This involves differencing the time series to make it stationary.
- **Moving Average (MA)**: The model exploits the relationship between the observation and the residual errors from a moving average model applied to lagged observations.

### Extending ARIMA to SARIMA for Seasonal Data
The Seasonal ARIMA, or SARIMA, model extends ARIMA by adding seasonal terms, which are crucial for modeling time series data with seasonal effects.

## Project Methodology:
### Project Architecture
![Project Architecture Image](https://drive.google.com/uc?export=view&id=YourImageID)
Our methodology encompasses several stages, from data gathering and preprocessing to modeling and evaluation, structured to facilitate systematic analysis and robust model development.

### Data Acquisition
- **Stock Data:** We collected historical data for Netflix from Yahoo Finance.
- **Twitter Data:** Tweets related to Netflix were extracted using the Snscrape tool over the same period.

### Data Cleaning
We processed the collected Twitter data by normalizing text, removing URLs, hashtags, emojis, and performing tokenization and lemmatization to prepare the data for analysis.

### Sentiment Analysis Implementation
![Sentiment Analysis Image](https://drive.google.com/uc?export=view&id=YourImageID)
We employed a pretrained model, `twitter-roberta-base-sentiment`, for categorizing tweets by sentiment, aiding in the assessment of public sentiment impact on stock prices.

### Data Integration
#### Preparing Data for ARIMA
This involved formatting the combined stock and sentiment data into a structure suitable for ARIMA modeling.

#### Preparing Data for CNN-LSTM
Data was organized into sequences to be used in the CNN-LSTM model, ensuring the structure supports temporal feature extraction and sequence learning.

### Model Development
#### ARIMA Modeling
![ARIMA Model Image](attachment:An_informative_graphic_depicting_the_structure_of_.png)
The ARIMA model was selected for its effectiveness in modeling and forecasting non-stationary time series data. We employed the Auto ARIMA process, which automates the selection of the best ARIMA model based on Akaike Information Criterion (AIC). The model iteratively explores various combinations of parameters (p, d, q) and integrates components (P, D, Q, S) for seasonal adjustments, ensuring the optimal fit for our time series data.

#### CNN-LSTM Model Design
![CNN-LSTM Model Image](attachment:A_sophisticated_digital_illustration_showing_a_Lon.png)
Our CNN-LSTM architecture combines the spatial feature extraction capabilities of CNNs with the sequential data processing strength of LSTMs. The model starts with one-dimensional convolutional layers that extract time-dependent features, followed by LSTM layers that model long-term dependencies in the data. This combination allows the model to capture complex patterns in the time series, essential for accurate forecasting. The model's performance is further enhanced by tuning hyperparameters such as the number of layers, filter sizes, and LSTM units to optimize prediction accuracy.

## Experimental Results
LSTM Training & Tdsting Accuracy 
![Results Image](https://drive.google.com/file/d/1cjh3KuW4NU6lgZvR_E7bpqI55L220cOm/view?usp=sharing)

## Conclusions:
The integration of sentiment analysis significantly enhances the predictability of stock price movements, demonstrating that our hybrid model not only matches but potentially exceeds traditional forecasting methods.

## Implementation Guide:
### How to Scrape Tweets
Instructions are provided for installing Snscrape and using it to gather tweets relevant to the stock market analysis.

### How to Perform Sentiment Analysis
Detailed steps are described for using the `twitter-roberta-base-sentiment` model to analyze the sentiment of scraped tweets.

## References and Further Reading

## Project Contributors
