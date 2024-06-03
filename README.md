# Stock Market Prediction Enhancement through Twitter Sentiment Analysis

## Table of Contents
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

## Introduction
![Sentiment](https://github.com/Vishwabhadiyadara/Sentiment-analysis-Netflix-stockmarket-Prediction/assets/110348340/e26bd3aa-429b-4e38-a8e3-10355d68d5da)

This project aims to enhance stock market predictions by integrating sentiment analysis from Twitter, recognizing that social media's influence and other unpredictable factors play significant roles in market movements.

## Conceptual Framework:
### The Role of CNN in Time Series Analysis
Convolutional Neural Networks (CNNs), especially 1D-CNNs, are adept at processing time series data, capturing essential patterns and reducing noise, thereby ideal for analyzing fixed-window time series data.

### The Application of LSTM in Time Series
Long Short-Term Memory (LSTM) networks excel in capturing long-term dependencies within time series data, making them particularly useful for predicting sequences in stock market trends.

![CNN-LSTM Image](https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs00521-020-04867-x/MediaObjects/521_2020_4867_Fig2_HTML.png)

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
![Picture5](https://github.com/Vishwabhadiyadara/EEG-Data-Classification-for-Neurological-Diagnosis/assets/110348340/6c8a49fa-c609-40fc-ad7b-e638e36f5843)

Our methodology encompasses several stages, from data gathering and preprocessing to modeling and evaluation, structured to facilitate systematic analysis and robust model development.

### Data Acquisition
- **Stock Data:** We collected historical data for Netflix from Yahoo Finance.
- **Twitter Data:** Tweets related to Netflix were extracted using the Snscrape tool over the same period.

### Data Cleaning
We processed the collected Twitter data by normalizing text, removing URLs, hashtags, emojis, and performing tokenization and lemmatization to prepare the data for analysis.

### Sentiment Analysis Implementation
We employed a pretrained model, `twitter-roberta-base-sentiment`, for categorizing tweets by sentiment, aiding in the assessment of public sentiment impact on stock prices.

### Data Integration
#### Preparing Data for ARIMA
This involved formatting the combined stock and sentiment data into a structure suitable for ARIMA modeling.

#### Preparing Data for CNN-LSTM
Data was organized into sequences to be used in the CNN-LSTM model, ensuring the structure supports temporal feature extraction and sequence learning.

### Model Development
#### ARIMA Modeling
The ARIMA model was selected for its effectiveness in modeling and forecasting non-stationary time series data. We employed the Auto ARIMA process, which automates the selection of the best ARIMA model based on Akaike Information Criterion (AIC). The model iteratively explores various combinations of parameters (p, d, q) and integrates components (P, D, Q, S) for seasonal adjustments, ensuring the optimal fit for our time series data.

#### CNN-LSTM Model Design
Our CNN-LSTM architecture combines the spatial feature extraction capabilities of CNNs with the sequential data processing strength of LSTMs. The model starts with one-dimensional convolutional layers that extract time-dependent features, followed by LSTM layers that model long-term dependencies in the data. This combination allows the model to capture complex patterns in the time series, essential for accurate forecasting. The model's performance is further enhanced by tuning hyperparameters such as the number of layers, filter sizes, and LSTM units to optimize prediction accuracy.

## Experimental Results
LSTM Training & Testing Accuracy 

![Picture1](https://github.com/Vishwabhadiyadara/Sentiment-analysis-Netflix-stockmarket-Prediction/assets/110348340/2c1d1470-2244-4579-8a06-a1a31082c88e) ![Picture2](https://github.com/Vishwabhadiyadara/Sentiment-analysis-Netflix-stockmarket-Prediction/assets/110348340/497bb673-5ab2-4a49-9f47-8fd49df0b9d6)

ARIMA Training & Testing Accuracy

![Picture3](https://github.com/Vishwabhadiyadara/Sentiment-analysis-Netflix-stockmarket-Prediction/assets/110348340/a186d111-1d41-4c51-9df0-14c3af835067) ![Picture4](https://github.com/Vishwabhadiyadara/Sentiment-analysis-Netflix-stockmarket-Prediction/assets/110348340/51454688-28cc-4b52-b7c9-df2f84f690c7)
## Conclusions:
This project has clearly demonstrated the significant potential of integrating sentiment analysis derived from social media with traditional stock market forecasting methods. By incorporating Twitter sentiment, our models were able to account for a broader spectrum of market-influencing factors, offering a more holistic view of potential market movements. Our CNN-LSTM model, in particular, showcased its robustness and superiority over conventional models like ARIMA, highlighting its capability to adapt and learn from complex datasets enriched with sentiment data. This approach not only enhances the precision of forecasts but also provides insights into the market's psychological landscape, which can be crucial for making informed investment decisions. Future work could explore the integration of other data types and the application of even more advanced machine learning techniques to further refine the accuracy and reliability of stock market predictions.

## Contact Details

- **Name**: Vishwa Bhadiyadara
- **Email**: [bhadiyadara.v@northeastern.edu](mailto:bhadiyadara.v@northeastern.edu)


