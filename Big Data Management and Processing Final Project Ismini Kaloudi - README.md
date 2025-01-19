
# Final Project – Ismini Kaloudi

The pyrhone code I have created for this project follows the below steps, in order to predict 
 the historical factors that have the most significant impact on cryptocurrency price movements, and potentially predict trends. 
1. Imports and Setup
Library Imports: Necessary libraries like pandas, numpy, matplotlib, seaborn, requests, and pymongo are imported for data manipulation, visualization, and database interaction.
MongoDB Connection: A connection is established to a MongoDB database called "Crypto" and a collection named "Cryptocurrency" to store the processed data.
2. Data Ingestion
Loading Data: A function load_data reads CSV files from a specified directory. All files in the directory that end with .csv are loaded into a single DataFrame (crypto_data).
Printing Data: The first few rows of the combined DataFrame are printed for inspection.
3. Data Cleaning and Transformation
The Date column is converted to a datetime format.
Duplicate rows are dropped, and missing values are handled with forward fill.
The cleaned DataFrame is converted to a dictionary format and inserted into the MongoDB collection.
4. Data Extraction and Analysis
Querying Data: An example query retrieves all records for Bitcoin (symbol: "BTC") from the MongoDB collection.
Price Movement Visualization: The closing price of Bitcoin over time is plotted using Matplotlib.
5. Daily Returns Analysis
Calculating Daily Returns: A new column for daily returns is created by calculating the percentage change in the closing price.
Visualizing Daily Returns: Daily returns are plotted in a second figure.
6. Advanced Data Processing
Loading and Cleaning Additional Data: The same23 CSV files are again read and concatenated into a single DataFrame. Missing values are checked and handled.
Average Closing Price Calculation: The script calculates and prints the average closing price for each cryptocurrency.
Visualization of Average Prices: A bar plot visualizes the average closing prices of different cryptocurrencies.
7. Correlation Analysis
A correlation matrix is generated to analyze relationships between price, volume, and market cap. This is visualized using a heatmap.
8. Predictive Modeling
Preparing Data for Regression: Features (Volume, High, Low, Open) and target variable (Close) are selected for regression modeling.
Train-Test Split: The data is split into training and testing sets.
Linear Regression Model: A linear regression model is fitted to the training data, and predictions are made on the test set. The mean squared error (MSE) of the predictions is printed.
9. Function Definitions
Functions for Loading and Cleaning Data: Custom functions are defined to load CSV files and clean the data by converting dates, renaming columns, and handling missing values.
Visualization Functions: Functions are created to plot price trends for individual cryptocurrencies and for multiple cryptocurrencies at once.
10. Visualization for Specific Cryptocurrencies
The script visualizes price trends for Bitcoin, Ethereum, Monero, and Uniswap using Plotly, which provides interactive graphs.
11. Prediction Columns:
For Bitcoin, Ethereum, Monero, and Uniswap, a new column named "Prediction" is created, which shifts the closing price by a specified number of projections (5 days ahead).
The closing, opening, high, low prices, and predictions for each cryptocurrency are plotted in separate line graphs.
Summary
Overall, this Python script is a robust framework for loading, cleaning, analyzing, and visualizing cryptocurrency data from multiple CSV files, each one for a different cryptocurrency. It integrates data storage in MongoDB, performs statistical analysis, builds a predictive model, and utilizes Plotly for interactive visualizations. The code is modular and can be adapted for further analysis or additional cryptocurrencies.
Datasets were extracted by Kaggle 
https://www.kaggle.com/datasets/sudalairajkumar/cryptocurrencypricehistory 

