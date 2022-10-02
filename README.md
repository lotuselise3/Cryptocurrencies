# Cryptocurrencies

## Overview
Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

## Purpose
- Describe the differences between supervised and unsupervised learning, including real-world examples of each.
- Preprocess data for unsupervised learning.
- Cluster data using the K-means algorithm.
- Determine the best number of centroids for K-means using the elbow curve.
- Use PCA to limit features and speed up the model.

## Results

**Deliverable 1: Preprocessing the Data for PCA**

Cleaned crypto_df DataFrame:
![Del1](https://user-images.githubusercontent.com/68654746/193461839-9396019e-3a86-43e0-9b32-3a14e2207318.png)

**Deliverable 2: Reducing Data Dimensions Using PCA**

Used the PCA algorithm to reduce the dimensions of the X DataFrame down to three principal components: 
![Del2](https://user-images.githubusercontent.com/68654746/193461930-55b41495-fdf6-4b87-9595-631384880bcb.jpg)

**Deliverable 3: Clustering Cryptocurrencies Using K-means**

Created an elbow curve using hvPlot to find the best value for K: 
![Del3_elbow](https://user-images.githubusercontent.com/68654746/193461994-4f8a2728-2490-4920-b1bd-ee9347cc6f0e.jpg)

Created a new DataFrame with the same index as the crypto_df DataFrame with the following columns added: 
Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class
![Del3](https://user-images.githubusercontent.com/68654746/193462040-c9883d8a-3171-4942-b633-19861485168b.jpg)

**Deliverable 4: Visualizing Cryptocurrencies Results**

Create a 3D scatter plot using the Plotly Express scatter_3d() function
![Del4_scatter](https://user-images.githubusercontent.com/68654746/193462768-311750cf-d984-45a7-a48f-e6d4d33b1b62.jpg)

Create a table with tradable cryptocurrencies
![Del4_table](https://user-images.githubusercontent.com/68654746/193462841-b66092df-f96f-49ae-b964-796940977af0.jpg)

Cleaned the clustered_df DataFrame index:

![Del4_updated_table](https://user-images.githubusercontent.com/68654746/193463014-9efa35d2-4ad5-436f-a2c1-21306ccd6e11.jpg)

Created an hvplot scatter plot with x="TotalCoinsMined", y="TotalCoinSupply", and by="Class": 

![image](https://user-images.githubusercontent.com/68654746/193463177-3bff1550-e996-454c-bab3-8f3844f0b556.png)
