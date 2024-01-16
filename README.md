# JPX-Tokyo-Stock-Exchange-Prediction

[Get the Dataset from Kaggle](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data)

# Dataset Description

This dataset contains historic data for a variety of Japanese stocks and options. Your challenge is to predict the future returns of the stocks.

As historic stock prices are not confidential, this will be a forecasting competition using the time series API. The data for the public leaderboard period is included as part of the competition dataset. Expect to see many people submitting perfect submissions for fun. Accordingly, the active phase public leaderboard for this competition is intended as a convenience for anyone who wants to test their code. The forecasting phase leaderboard will be determined using real market data gathered after the submission period closes.

## Files

- **stock_prices.csv**: The core file of interest. Includes the daily closing price for each stock and the target column.
- **options.csv**: Data on the status of a variety of options based on the broader market. Many options include implicit predictions of the future price of the stock market and so may be of interest even though the options are not scored directly.
- **secondary_stock_prices.csv**: The core dataset contains on the 2,000 most commonly traded equities but many less liquid securities are also traded on the Tokyo market. This file contains data for those securities, which aren't scored but may be of interest for assessing the market as a whole.
- **trades.csv**: Aggregated summary of trading volumes from the previous business week.
- **financials.csv**: Results from quarterly earnings reports.
- **stock_list.csv**: Mapping between the SecuritiesCode and company names, plus general information about which industry the company is in.

## Folders

- **data_specifications/**: Definitions for individual columns.
- **jpx_tokyo_market_prediction/**: Files that enable the API. Expect the API to deliver all rows in under five minutes and to reserve less than 0.5 GB of memory.

Copies of data files exist in multiple folders that cover different time windows and serve different purposes.

- **train_files/**: Data folder covering the main training period.
- **supplemental_files/**: Data folder containing a dynamic window of supplemental training data. This will be updated with new data during the main phase of the competition in early May, early June, and roughly a week before the submissions are locked. The supplemental data will also be updated once at the very beginning of the forecasting phase so that the test set will start with the trading day after the last trading day in the supplemental data.
- **example_test_files/**: Data folder covering the public test period. Intended to facilitate offline testing. Includes the same columns delivered by the API (i.e., no Target column). You can calculate the Target column from the Close column; it's the return from buying a stock the next day and selling the day after that. This folder also includes an example of the sample submission file that will be delivered by the API.
