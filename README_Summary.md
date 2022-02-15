# Unit 13 Homework Assignment - The Power of the Cloud and Unsupervised Learning

## Background

For this assignment, I have completed the Option 2 Challenge: Clustering Crypto.

## Clustering Crypto

![Cryptocurrencies coins](Images/cryptocurrencies-coins.jpg)
_[Cryptocurrencies coins by Worldspectrum](https://www.pexels.com/@worldspectrum?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) | [Free License](https://www.pexels.com/photo-license/)_

### Background

You are a Senior Manager at the Advisory Services team on a [Big Four firm](https://en.wikipedia.org/wiki/Big_Four_accounting_firms). One of your most important clients, a prominent investment bank, is interested in offering a new cryptocurrencies investment portfolio for its customers, however, they are lost in the immense universe of cryptocurrencies. They ask you to help them make sense of it all by generating a report of what cryptocurrencies are available on the trading market and how they can be grouped using classification.  

In this homework assignment, I have put my new unsupervivsed learning and Amazon SageMaker skills into action by clustering cryptocurrencies and creating plots to present my results.

I have accomplished the following main tasks:

* **[Data Preprocessing](#Data-Preprocessing):** Prepare data for dimension reduction with PCA and clustering using K-Means.

  - Example of - Cleaned Data Frame

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/clean_df.PNG?raw=true)

  - Example of - Cleaned Data Scaled

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/clean_scaled_df.PNG?raw=true)

* **[Reducing Data Dimensions Using PCA](#Reducing-Data-Dimensions-Using-PCA):** Reduce data dimension using the `PCA` algorithm from `sklearn`.

  - Example of - Data Reduced using PCA

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/pcs_df.PNG?raw=true)

* **[Clustering Cryptocurrencies Using K-Means](#Clustering-Cryptocurrencies-Using-K-Means):** Predict clusters using the cryptocurrencies data using the `KMeans` algorithm from `sklearn`.

  - Predictions using K-Means for K = 1-11

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Elbow_Curve.PNG?raw=true)

* **[Visualizing Results](#Visualizing-Results):** Create some plots and data tables to present your results.

  - Visualisation for Clusters (TotalCoinsMined vs TotalCoinsSupply)

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Clusters_TCM_vs_TCS.png?raw=true)

  - Table visualisation for Coins and Clusters

   ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/crypto_class_table.PNG?raw=true)

* **[Visualizing Results Extra](#Visualizing-Results):**

I created some additional visualisations which I thought gave further insight and meaning to the clustering of this data. 

  - View 1 - Additional 3D Visualisationd for Clusters (PCS 1, PCS 2 and PCS 3)

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Clusters_PC1_PC2_PC3_view1.png?raw=true)

  - View 2 - Additional 3D Visualisationd for Clusters (PCS 1, PCS 2 and PCS 3)

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Clusters_PC1_PC2_PC3_view2.png?raw=true)


* **[Optional Challenge](#Optional-Challenge):** Deploy your notebook to Amazon SageMaker.

The challenge for this homework assignment has been completed and the crypto_clustering_sm.ipynb notebook has been deployed to Amazon Sagemaker. All visualisation have been converted to use the Altair library and all references to hvplot have been removed. Below are images captured for all visualisations created by the Notebook deployed on AWS SageMaker.

  - Use the altair scatter plot to create the Elbow Curve.

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/altair_elbow_curve.png?raw=true)

    - Use the altair scatter plot to visualize the clusters. Since this is a 2D-Scatter, use x="PC 1" and y="PC 2" for the axes, and add the following columns as tool tips: "CoinName", "Algorithm", "TotalCoinsMined", "TotalCoinSupply".

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Altair_Clusters_PC1_vs_PC2.png?raw=true)

    - Use the altair scatter plot to visualize the tradable cryptocurrencies using  x="TotalCoinsMined" and y="TotalCoinSupply" for the axes.

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/Altair_Clusters_TCM_vs_TCS.png?raw=true)

      - Show the table of current tradable cryptocurrencies using the display() command.

  ![](https://github.com/apfreeman/unit13-challenge/blob/main/Images/crypto_class_table_using_display.PNG?raw=true)

