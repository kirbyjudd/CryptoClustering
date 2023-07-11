# CryptoClustering

## Module 19 Challenge
In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

### 1. Prepare the Data
- The first task was to scale the data using the 'StandardScaler()' module from sci-kit learn. After normalizing the data from the CSV file, I created a dataframe with the scaled data called "df_market_scaled". The index was set to the "coin_id" column.

### Find the Best Value for k Using the Original Scaled DataFrame
- Next, I used the elbow method in order to find the best value for k by creating the k values list from 1 to 11, and an empty list called inertia to store the inertia values. Using a for loop, I computed the inertia with each possible value of k. After plotting the elbow curve, it was decided that 4 clusters would be the best value for k.
  
### 2. Cluster Cryptocurrencies with K-means Using the Original Scaled Data
- Now that I had to best value for k, I could use the K-mean model to predict the clusters that would be grouped. I added the cluster column to a copy of the df_market_scaled dataframe and plotted the predictions using hvplot.

### 3. Optimize Clusters with Principal Component Analysis
- Next, I would use Principal Component Analysis in order to reduce the number of features to three principal components. The total explained variance of the three principal components turned out to be around 89.5%. 

### 4. Find the Best Value for k Using the PCA Data
- I then created another elbow curve for the PCA data and found the the best value for k was still 4 clusters which did not differ from the original data.

### 5. Cluster Cryptocurrencies with K-means Using the PCA Data
- I used the K means model again to predict the cluster that would be grouped. I then added the cluster column to the PCA predictions dataframe and plotted the PCA scatter plot.
  
### 6. Visualize and Compare the Results
- I combined both elbow curves together in order to compare and contrast the elbow curves. They were both very similar visually, which is why both had an optimal k value of 4.
- Likewise, I combined both Original and PCA scatter plots in order to compare and contrast. The PCA model uses fewer features than the K-Means model which creates a more tight and compact group of clusters. Using fewer features to cluster the data allows for more distinct cluster to be seen.  This could allow for better understanding of the clusters as there will be fewer features that may complicate the analysis. 

### Peer Cooperation
- I worked together on this assignment with my classmate Riddhi Sodagar.
  
### File locations
- The main jupyter notebook is called "Crypto_Clustering.ipynb" and is located in main.
- The graphs were not showing up on GitHub so I saved all of the hvplot graphs to a folder called "Images". 
