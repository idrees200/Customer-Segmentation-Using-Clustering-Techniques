# Customer Segmentation Using Clustering Techniques

## Overview

This repository contains Python scripts for clustering analysis on an Online Retail dataset using KMeans and Agglomerative Clustering algorithms. The goal is to segment customers based on their purchasing behavior, specifically focusing on the features Quantity and UnitPrice.

## Dataset

The dataset (`OnlineRetail.csv`) consists of transaction records including details such as quantity of items purchased (`Quantity`), unit price of items (`UnitPrice`), and other transaction information.

## Code Explanation

1. **Data Loading and Cleaning**
   - The dataset is loaded into a pandas DataFrame (`data`).
   - Initial inspection with `data.head()` and `data.isnull().sum()` reveals the structure and any missing values.
   - Data cleaning includes removing rows with outliers using z-score filtering (`scipy.stats.zscore`).

2. **KMeans Clustering**
   - Data scaling is performed using `StandardScaler` from `sklearn.preprocessing`.
   - The Elbow Method is applied to determine the optimal number of clusters (`KMeans.inertia_`).
   - KMeans clustering is then applied with the optimal number of clusters, and results are visualized using a scatter plot (`sns.scatterplot`).

3. **Hierarchical (Agglomerative) Clustering**
   - Data sampling is implemented to manage memory constraints, if necessary.
   - Hierarchical clustering is performed using `AgglomerativeClustering` from `sklearn.cluster`.
   - Results are visualized similarly to KMeans clustering with a scatter plot.

4. **Dendrogram Visualization**
   - A dendrogram is generated using `scipy.cluster.hierarchy.dendrogram` to visualize the hierarchical clustering process.

## Usage

Ensure Python environment is set up with necessary libraries (`pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`, `scipy`). Run the script to load the dataset, perform clustering using both KMeans and Agglomerative methods, and visualize the results.

## Improvements

- Explore other clustering algorithms (e.g., DBSCAN, Gaussian Mixture Models) for comparison.
- Conduct further feature engineering or selection to enhance clustering accuracy.
- Optimize memory usage for handling larger datasets.
![Screenshot 2024-06-23 201947](https://github.com/idrees200/Customer-Segmentation-Using-Clustering-Techniques/assets/113856749/437364ed-64e9-4718-b13a-fe43184f04ad)
![Screenshot 2024-06-23 201943](https://github.com/idrees200/Customer-Segmentation-Using-Clustering-Techniques/assets/113856749/2b055516-fb36-4faa-a7c0-e9918de3cbf7)
![Screenshot 2024-06-23 201938](https://github.com/idrees200/Customer-Segmentation-Using-Clustering-Techniques/assets/113856749/352360a7-080f-4191-b635-0d86a3a88d18)
![Screenshot 2024-06-23 201953](https://github.com/idrees200/Customer-Segmentation-Using-Clustering-Techniques/assets/113856749/5f58c97b-44f3-40b6-a6e2-3824903c668d)

