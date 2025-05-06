# Clustering Analysis on Auto-MPG, Boston Housing, and Wine Datasets

## Overview

This project explores the application of hierarchical clustering and K-Means clustering algorithms to uncover underlying structures in three different datasets: the Auto-MPG dataset, the Boston Housing dataset, and the Wine dataset. The primary goal is to identify natural groupings within the data and assess the relationships between these clusters and known class labels, where applicable.

## Datasets

*   **Auto-MPG Dataset:** Sourced from the UCI Machine Learning Repository, this dataset contains information on automobile fuel efficiency along with attributes such as displacement, horsepower, weight, and origin. The task involves clustering based on continuous features to reveal groupings of automobiles and their correlation with geographic origin.

*   **Boston Housing Dataset:** Also from the UCI Machine Learning Repository, this dataset includes various attributes of houses in the Boston area, such as per capita crime rate, average number of rooms, and tax rates. K-Means clustering is used to identify groupings of houses and their relationships with key variables like the median house price (MEDV).

*   **Wine Dataset:** Available from the UCI Machine Learning Repository via scikit-learn, this dataset comprises chemical analysis results of wines from three different cultivars in Italy. K-Means clustering is applied to discover groupings of wines, and clustering quality is evaluated using homogeneity and completeness metrics with respect to the actual cultivar types.

## Methodology

*   **Hierarchical Clustering (Auto-MPG Dataset):**
    *   Utilized `sklearn.cluster.AgglomerativeClustering` with the `average` linkage criterion and Euclidean distance as the affinity metric.
    *   The number of clusters was set to 3.
*   **K-Means Clustering (Boston Housing Dataset):**
    *   Implemented using `sklearn.cluster.KMeans`.
    *   The optimal number of clusters was determined by calculating silhouette scores for a range of cluster numbers (2 to 6).
    *   Features were standardized using `StandardScaler`.
*   **K-Means Clustering (Wine Dataset):**
    *   Applied `sklearn.cluster.KMeans` with a fixed number of clusters (n\_clusters = 3) to the scaled dataset.
    *   Clustering quality was evaluated using Homogeneity and Completeness metrics from `sklearn.metrics`.

## Results and Analysis

### Auto-MPG Dataset

*   Analyzed mean and variance of features within each cluster.
*   Compared clustering results with the `origin` class label.
*   Observations: Cluster 1 exhibited a strong correlation with Origin 1, while Cluster 0 showed a mixed composition of all origins. Cluster 2 showed a strong correlation with Origin 2.

### Boston Housing Dataset

*   Determined the optimal number of clusters based on silhouette scores.
*   Computed and analyzed cluster feature means and centroid coordinates.
*   Observations: k=2 yielded a good clustering result, with crime rate and distance to employment centers being key differentiators.

### Wine Dataset

*   Calculated homogeneity and completeness scores to assess clustering quality.
*   The homogeneity and completeness scores are as follows:
    *   Homogeneity: 0.8788
    *   Completeness: 0.8730
*   Observations: High homogeneity and completeness scores suggest that the K-Means clustering effectively grouped wines according to their cultivar types.

## Key Findings

*   The hierarchical clustering on the Auto-MPG dataset revealed partial correlations between cluster assignments and car origins.
*   The K-Means clustering on the Boston Housing dataset identified groupings of houses differentiated by crime rates and proximity to employment centers.
*   The K-Means clustering on the Wine dataset demonstrated high accuracy in grouping wines by their cultivar types, as indicated by the homogeneity and completeness scores.

## Dependencies

*   Python 3.x
*   scikit-learn
*   pandas
*   matplotlib
*   seaborn

## Usage

1.  Clone this repository.
2.  Ensure all dependencies are installed (`pip install scikit-learn pandas matplotlib seaborn`).
3.  Run the appropriate scripts for each dataset to reproduce the results.

For specific details, please refer to Homework4.0-Report
