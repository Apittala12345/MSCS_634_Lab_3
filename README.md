# MSCS 634 - Lab 3: Clustering Using K-Means and K-Medoids

## Purpose

The purpose of this lab is to explore and compare K-Means and K-Medoids clustering techniques using the Wine Dataset from the sklearn Python library.

The dataset was standardized using z-score normalization before clustering. Both algorithms were implemented with 3 clusters because the Wine dataset contains 3 known classes.

The clustering performance was evaluated using:
- Silhouette Score
- Adjusted Rand Index (ARI)

## Key Results

### K-Means
- Silhouette Score: 0.2849
- Adjusted Rand Index (ARI): 0.8975
- Cluster 0: 65 samples
- Cluster 1: 51 samples
- Cluster 2: 62 samples

### K-Medoids
- Silhouette Score: 0.2660
- Adjusted Rand Index (ARI): 0.7263
- Cluster 0: 51 samples
- Cluster 1: 54 samples
- Cluster 2: 73 samples

## Key Insights

K-Means performed better than K-Medoids on the Wine dataset.

K-Means achieved a higher Silhouette Score, which indicates slightly better cluster separation and compactness.

K-Means also achieved a higher ARI, showing that its clusters matched the actual Wine class labels more closely than the K-Medoids clusters.

The visualizations showed that both algorithms identified similar overall groupings, although some points near cluster boundaries were assigned differently.

## K-Means vs. K-Medoids

K-Means uses calculated centroids as cluster centers and works well for numeric datasets that are reasonably clean.

K-Medoids uses actual data points as cluster centers and is generally more robust to outliers.

## Challenges and Decisions

One challenge was ensuring that all features were on the same scale before clustering. StandardScaler was used to apply z-score normalization.

The `scikit-learn-extra` package was used to implement K-Medoids.

PCA was used to reduce the standardized dataset to two dimensions for visualization.

The number of clusters was set to 3 because the Wine dataset contains 3 known classes.

Windows-specific threading warnings were handled by setting environment variables before running the clustering algorithms.

## Conclusion

Both K-Means and K-Medoids successfully produced meaningful clusters on the Wine dataset. However, K-Means performed better based on both the Silhouette Score and Adjusted Rand Index.
