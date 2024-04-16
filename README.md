# stock_market_prediction
This project focuses on predicting stock market prices using a combination of historical stock data and sentiment analysis of news headlines. The main steps involved in the project are:

Importing Libraries: Libraries such as NumPy, Pandas, Matplotlib, TextBlob, VaderSentiment, and others are imported to facilitate data manipulation, sentiment analysis, and LSTM model creation.

Loading Dataset: Two datasets are loaded, one containing historical stock market data (update_data.csv) and the other containing news headlines (Combined_News_DJIA(train).csv).

Plotting Target Variable: The closing prices from the historical stock data are plotted to visualize the price history.

Merging Datasets: Both datasets are merged on the 'Date' column to combine historical stock data with corresponding news headlines.

Cleaning Headlines: The headlines are cleaned to remove unnecessary characters and make them suitable for analysis.

Sentiment Analysis: Sentiment analysis is performed on the cleaned headlines to extract subjectivity and polarity, which can help gauge the sentiment of the news.

Adding Sentiment Scores: Sentiment scores (compound, negative, positive, neutral) are added to the merged dataset based on the sentiment analysis of the headlines.

Feature Extraction: Relevant features including 'Date', 'Open', 'High', 'Low', 'Volume', and sentiment scores are selected for further analysis.

Train/Valid Split: The dataset is split into training and validation sets for model training.

Creating Window Size: A window size of 60 is created for LSTM modeling.

Scaling the Data: Data is scaled using MinMaxScaler to ensure all features are on a similar scale.

Creating LSTM Model: An LSTM model is created using Keras with 50 units and compiled with the Adam optimizer.

Creating Valid Data: Data for validation is prepared using the same steps as for training data.

Predicting Closing Prices: Closing prices are predicted using the trained LSTM model.

Plotting Predictions: Predicted closing prices are plotted along with actual closing prices for visualization.

Loading Test Data: Test data containing news headlines (Test_Combined_News.csv) and stock market data (Test_DJIA_Table.csv) are loaded for prediction.

Generating Predictions for Test Data: Predictions are made for the test data using the trained LSTM model.

Saving Predictions: Predictions are saved to a CSV file (asd.csv) for further analysis.

Trading Decision: Based on the predicted closing price, a trading decision (Buy, Sell, Hold) is made for the next day.

