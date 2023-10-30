# CryptoClustering

1. Imported the required libraries and dependencies.

2. Loaded the data into a Pandas DataFrame.

3. Generated the summary statistics

4. Plotted the data to see what's in the DataFrame

![market_data_plot](https://github.com/aclima88/CryptoClustering/assets/133547307/cffa0bb4-9500-4958-aaf5-9e4b2fb687f5)

# Prepare the Data.

5. Used the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file.

6. Created a DataFrame with the scaled data

7. Copied the crypto names from the original data and set the coinid column as the index.

# Find the Best Value for k Using the Original Data.

8. Created a list with the number of k-values from 1 to 11.

9. Created an empty list to store the inertia values.

10. Created a for loop to compute the inertia with each possible value of k.
	a. Created a KMeans model with k clusters.
	b. Fit the model to the scaled data.
	c. Appended the model's inertia to the inertia list.

11. Created a dictionary with k-values as keys and their corresponding inertia values.
	a. Created a DataFrame with the data for plotting the Elbow curve.

12. Plotted a line chart with all the inertia values computed with  the different values of k to visually identify the optimal value for k.

![elbow_curve](https://github.com/aclima88/CryptoClustering/assets/133547307/2ffce1fb-b4f3-4e9c-bd6e-73027fea3693)

# Cluster Cryptocurrencies with K-means Using the Original Data

13. Initialized the K-Means model using the best value for k.

14. Fit the K-Means model using the scaled data.

15. Predicted the clusters to group the cryptocurrencies using the scaled data.

16. Created a scatter plot using the data.

![scatter_plot](https://github.com/aclima88/CryptoClustering/assets/133547307/2227890a-6fbe-4dce-8426-b0af904d4789)

# Optimize Clusters with Principal Component Analysis.

17. Created a PCA model instance and set `n_components=3`.

18. Used the PCA model with `fit_transform` to reduce to three principal components.

19. Retrieved the explained variance to determine how much information can be attributed to each principal component.

20. Created a new DataFrame with the PCA data.
	a. Set the coinid column as index

![PCA_dataframe](https://github.com/aclima88/CryptoClustering/assets/133547307/d041a440-d01d-48b0-8848-c09b82e8f61b)

# Find the Best Value for k Using the PCA Data

21. Created a list with the number of k-values from 1 to 11.

22. Created an empty list to store the inertia values.

23. Create a for loop to compute the inertia with each possible value of k.
	a. Created a KMeans model using the loop counter for the n_clusters.
	b. Fit the model to the data using `df_market_pca`.
	c. Append the model.inertia_ to the inertia list.

24. Created a dictionary with the data to plot the Elbow curve.
	a. Created a DataFrame with the data to plot the Elbow curve.

25. Plotted a line chart with all the inertia values computed with  the different values of k to visually identify the optimal value for k.

![PCA_elbow_curve](https://github.com/aclima88/CryptoClustering/assets/133547307/70fe5e41-1be5-45b2-9d09-7511440113f6)

# Cluster Cryptocurrencies with K-means Using the PCA Data

26. Initialized the K-Means model using the best value for k.

27. Fit the K-Means model using the PCA data.

28. Predicted the clusters using the K-Means model.

29. Added a new column to the DataFrame with the predicted clusters.

![predicted_clusters_df](https://github.com/aclima88/CryptoClustering/assets/133547307/4dc1489a-9de3-4717-b501-268e9076c3a6)

30. Create a scatter plot to display the PCA clusters.

![PCA_scatter_plot](https://github.com/aclima88/CryptoClustering/assets/133547307/0e4ba279-266f-4d4a-ab14-9667cdc66ddb)

# Visualize and Compare the Results

31. Created a figure with two subplots (for the original and PCA data) to contrast the Elbow curves.

![elbow_curve_contrast](https://github.com/aclima88/CryptoClustering/assets/133547307/122a6d0a-da66-4a00-b271-110d21475d81)

32. Created a scatter plot for the original dataset to contrast the clusters.

![scatter_plot_contrast](https://github.com/aclima88/CryptoClustering/assets/133547307/c54dfd29-fc92-443c-b206-8fb42b6518b8)
 





