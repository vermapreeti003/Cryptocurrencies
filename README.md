# Cryptocurrencies

## Overview

Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. In this project, we are going to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

Since the data is not ideal, it will need to be processed to fit the machine learning models. Moreover, since there is no known output for what we are looking for, we have decided to use unsupervised learning and clustering algorithm. Finally, we will use data visualizations to share the findings.

### Aim
The aim of this project is to create an analysis to find what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for a new investment.

## Analysi of Data

### Preprocessing the Data
As first step, we have loaded the data (Table 1) and we have preprocessed it to get the DataFrame of Table 2


![st1](https://user-images.githubusercontent.com/111541268/211165409-01238535-ac8e-427d-bb29-b2abef4e6682.png)
   
   Table1: DataFrame of original Data




![st2](https://user-images.githubusercontent.com/111541268/211165422-64034689-4d06-4667-a53c-1a1091c295ed.png)
    
    Table 2: Preprocessed Data
      
### Reducing Data Dimensions Using PCA

As a second step, we have applied the Principal Component Analysis (PCA) algorithm to reduce the dimensions of the DataFrame to three principal components and place these dimensions in a new DataFrame named pcs_df.


![st3](https://user-images.githubusercontent.com/111541268/211165493-e066b555-21e4-473a-a968-76f41673c73c.png)

### Clustering Cryptocurrencies Using K-means
As third step, we have:

 * Used a K-means algorithm to create an elbow curve using hvplot to find the best value for K from the pcs_df DataFrame created in the second step.
 * Ran the K-means algorithm to predict the K clusters for the cryptocurrencies’ data and be able to create a new DataFrame including predicted clusters and              cryptocurrencies features. This new DataFrame was named clustered_df.
 
 
 ![st8](https://user-images.githubusercontent.com/111541268/211166024-64305cfc-e83d-431e-bbea-a5ac9a2ef524.png)
      
      Fig: Elbow Curve
 
 
 ![st7](https://user-images.githubusercontent.com/111541268/211166026-48c845f8-2490-41dd-93b6-addf9f7aedf2.png)

      Table: DataFrame including predicted clusters and cryptocurrencies features
 
 
### Visualizing Cryptocurrencies Results
In the last step we have:

 * Created scatter plots with Plotly Express and hvplot, to visualize the distinct groups that correspond to the three principal components created in step 2. 
 * Created a table with all the currently tradable cryptocurrencies hvplot.table() function
 * Scaled the data, created a new DataFrame that has the scaled data to create hvplot.scatter plot of TotalCoinsMined versus TotalCoinSupply by Class. 


![st4](https://user-images.githubusercontent.com/111541268/211165703-6d2237cf-e247-4f44-9de8-1f54bb5f2723.png)
         Fig: 3D scatter plot of clusters




![st5](https://user-images.githubusercontent.com/111541268/211165709-f47d85b9-f42f-4991-814a-481bfeb23506.png)

Table: Currently tradable crypotcurrencies




![st6](https://user-images.githubusercontent.com/111541268/211165719-a1450796-2053-4b46-88a3-9b9daa9cac3e.png)
    Fig: 2D scatter plot of clusters



