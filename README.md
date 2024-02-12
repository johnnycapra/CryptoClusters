# Cryptocurrency Clustering Analysis Instructions

## 1. Prepare the Data

### Normalizing the Data
- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
- Create a DataFrame with the scaled data.
- Set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Finding the Best Value for k Using the Original Scaled DataFrame

#### Elbow Method
- Create a list with the number of k values from 1 to 11.
- Create an empty list to store the inertia values.
- Compute the inertia with each possible value of k using the K-means algorithm.
- Plot a line chart with the inertia values to visually identify the optimal value for k.
- Answer the question: What is the best value for k?

### Clustering Cryptocurrencies with K-means Using the Original Scaled Data

- Initialize the K-means model with the best value for k.
- Fit the K-means model using the original scaled DataFrame.
- Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
- Create a copy of the original data and add a new column with the predicted clusters.
- Create a scatter plot using hvPlot:
  - Set the x-axis as "PC1" and the y-axis as "PC2".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## 2. Optimize Clusters with Principal Component Analysis (PCA)

- Perform PCA on the original scaled DataFrame to reduce the features to three principal components.
- Retrieve the explained variance to determine the total explained variance of the three principal components.
- Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame.
- Use the elbow method on the PCA data to find the best value for k.
- Cluster the cryptocurrencies using K-means and the PCA data.
- Create a scatter plot using hvPlot:
  - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
  
## Conclusion

By following these instructions, you will perform clustering analysis on cryptocurrency data to identify patterns and clusters within the data. This analysis will provide valuable insights for investors and researchers in the cryptocurrency market.
# CryptoClusters
