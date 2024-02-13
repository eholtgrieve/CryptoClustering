# CryptoClustering

# Instructions
- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
- Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
  - What is the total explained variance of the three principal components?
- Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

The first five rows of the PCA DataFrame should appear as follows:
![image](https://github.com/eholtgrieve/CryptoClustering/assets/140793574/a807d99d-e13b-499f-9171-b9021f773868)


- Find the Best Value for k Using the PCA Data
   - Use the elbow method on the PCA data to find the best value for k using the following steps:
   - Create a list with the number of k-values from 1 to 11.
   - Create an empty list to store the inertia values.
   - Create a for loop to compute the inertia with each possible value of k.
   - Create a dictionary with the data to plot the Elbow curve.
   - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
   - Answer the following question in your notebook:
       - What is the best value for k when using the PCA data?
       - Does it differ from the best k value found using the original data?

- Cluster Cryptocurrencies with K-means Using the PCA Data
   - Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
     - Initialize the K-means model with the best value for k.
     - Fit the K-means model using the PCA data.
     - Predict the clusters to group the cryptocurrencies using the PCA data.
     - Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
    - Create a scatter plot using hvPlot as follows:
    - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
    - Color the graph points with the labels found using K-means.
    - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
    - Answer the following question:
       - What is the impact of using fewer features to cluster the data using K-Means?
    
# Results
- What is the total explained variance of the three principal components?:
  - The total explained variance of the three principal components is 0.47862164 + 0.26608254 + 0.1684978 = 0.9132019782433117.
- What is the best value for k when using the PCA data?:
   - The best value for k when using the PCA data is 4.
- Does it differ from the best k value found using the original data?:
    - This value does not differ from the best k value found with the original data.
- What is the impact of using fewer features to cluster the data using K-Means?:
   - The impact of having fewer features is a postive one since it creates clusters that are better defined which leads to more accurate cluster results.
