# Capstone: Bitcoin: Time Series Forecasting Using Machine Learning
---
## Problem Statement
---
This project examined Bitcoin data in order to create an accurate forecasting model for Bitcoin prices. Both on-chain (Bitcoin protocol data) and off-chain (market data) were used to analyze important factors and their relationship with the asset price. Underlying hypothesis was that fundamental factors of the Bitcoin blockchain may hold predictive power for future prices. The goal of this project can be summarized by the following problem statement:

- Given a  time series of Bitcoin prices and data, can we accurately predict future prices? How accurately?

The data was pulled from two sources: Glassnode and Coinmetrics.

Various models were used for time-series forecasting:

- SARIMA and SARIMAX
- Facebook Prophet
- LSTM RNN

Other models used for regression and feature extration were:

- Linear Regression, Extra Trees and Logistic Regression

Bitcoin -- Important Facts:

- Created in January 3rd, 2009 by Satoshi Nakamoto
    - “Bitcoin: A Peer- to-Peer Electronic Cash System”
- Bitcoin protocol and blockchain:
    - Distributed ledger that maintains the balances of all token trading (data!)
    - Decentralized (no central authority)
    - Transparent
    - Immutable
    - Cheap and Fast
    - Pseudo-anonymous
- Bitcoin token: 
    - Unit of the digital currency that users own and trade. A bitcoin token is held in a bitcoin wallet (wallet address and key)
- Mining and Cryptography:
    - Miners compete to do complex mathematical computations in order to get block reward (bitcoins!) every 10 minutes
    - Block reward is fixed: was 12.5 now is half: 6.25 bitcoins per block
- Bitcoin Halving:
    - Occurs every 210,000 blocks
    - Block reward is halved (July 2016, May 2020, 2024)
    - Hard-coded limit of 21 million bitcoins
- Supply/demand imbalance:
    - Increase in price
- Proven Scarcity: Digital Gold narrative

## Executive Summary
---
To investigate trends and structures in the Bitcoin dataset from the Glassnode and Coinmetrics APIs, we analyzed features that in theory could have impact on prices, investigated trends, created data visualizations to assist in our understanding of the data, then ran time series SARIMA models, Facebook Prophet and deep learning models with LSTM RNNs to inform and communicate our findings.

Data Gathering:

- Created custom functions to pull from Glassnode and Coinmetrics' API
- Ran pull request functions to gather a reasonable amount of data to run insightful models

Exploratory Data Analysis:

- Explored the distribution of key features and their relationship to price
- Analyzed fundamental metrics such as addresses, mining revenue, hashing difficulty and others.
- Used correlation matrices to gain more understanding of potential explanatory and predictive variables

Cleaning and Preprocessing:

- Engineered new columns for title, post and comment lengths
- Properly imputed missing data with correct numerical values
- Merged dataframes into a single dataframe for modeling
- Dropped unecessary columns and otherwise prepared dataset for each respective model

Visualizations:

- Created plots to visualize relationship of potential key variables with price
- Overlayed bitcoin halving dates to infer its impact on price.

Time Series and Deep Learning Models:

- Created univariate and multivariate models for SARIMA(X), Facebook Prophet and LSTM RNNs
- Fine tuned various hyperparameter and network structures for each model
- Used appropriate performance metrics for each model

Conclusions and Further Developments:

- The Facebook Prophet model performed the best amongst the forecasting models
- Bitcoin price is predicted to go up to over $20,000 in the next months
- Would complement the project by further tuning RNN model, use hourly data for bigger dataset and improve feature selection process