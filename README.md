# CryptoCurrencies

# Overview:
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

# Requirements:

1. Preprocessing the Data for PCA
2. Reducing Data Dimensions Using PCA
3. Clustering Cryptocurrencies Using K-means
4. Visualizing Cryptocurrencies Results

# Preprocessing Data:

1. Using the provided CSV file, open and read the file data directly into a DataFrame named crypto_df

2. Keep only the necessary columns: 'CoinName','Algorithm','IsTrading','ProofType','TotalCoinsMined','TotalCoinSupply'

3. Keep only the cryptocurrencies that are trading and with a working algorithm.

4. Remove the IsTrading column.

5. Remove all cryptocurrencies with at least one null value.

6. Keep rows where coins are mined.

7. Store the names of all cryptocurrencies in a new DataFrame using the index of crypto_df. 

8. Remove the CoinName column from original dataframe.

9. Create dummy variables for all the text features.

10. Use the StandardScaler from sklearn to standardize all the data of dummy variables.


# Reducing Data Dimensions Using PCA

Use the PCA algorithm from sklearn to reduce the dimensions down to three principal components. Once you have reduced the data dimensions, create a DataFrame using as columns names "PC 1", "PC 2" and "PC 3"; use the crypto_df.index as the index for this new DataFrame.

# Clustering Cryptocurrencies Using K-means

Create an Elbow Curve to find the best value for k using pca DataFrame. Once defined the best value for k, run the Kmeans algorithm to predict the k clusters for the cryptocurrencies data. Use the pca dataframe to run the KMeans algorithm. Create a new DataFrame named clustered_df and for this dataframe concatenate crypto_df and pca_df to include all data in one dataframe.

# Visualizing Cryptocurrencies
1. Create a 3D scatter plot

2. Use hvplot.table to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: "CoinName", "Algorithm", "ProofType", "TotalCoinSupply", "TotalCoinsMined", "Class"

3. Create a new DataFrame that has the scaled data with the clustered_df DataFrame index and add new columns "CoinName" and "Class".

 
