# Crypto Currencies
Analyze different cryptocurrencies to extrapolate common patterns and factors for investment firms looking to *invest* in cryptocurrency.

Using unsupervised machine learning models and algorithms on collections of cryptocurrencies to find patterns when a target feature is missing or and all features unlabeled. The primarily algorithm, K-means, will group similar data of cryptocurrency features into clusters. In addition, PCA (Principal Component Analysis) which helps reduce features and avoid overfitting data.  

Here is a rundown of Unsupervised Machine Learning practice: 

- Understand both supervised and unsupervised learning
- Preprocess data for unsupervised learning with Pandas ```pd.get_dummies```, with training and testing for algorithm processing
- Cluster data using the K-means algorithm with *K* number of clusters with means of data appointed to each cluster
- Determine the best number of centroids clusters for K-means using the elbow-point curve and inertia objective function which measures variation in the dataset
- Use PCA to limit features, avoid overfitting data, and speed up the model by transforming a larger set of variables into a digestible formed set.
- Hierarchical clustering, aka agglomerative clustering, can be used in tandem with K-means that groups (clusters) data points

## Unsupervised Machine Learning Practice Datasets
Selected datasets were cleaned and transformed in various methods such as removing null values and duplicates, removing textual-based and ID based columns, and boolean statement data points into strings. These transformations indicate pattern for digestible data for a number-crunching machine, such as a laptop, to perform machine learning.
![data1](unsuperised_pracitice_notebooks\img\transformed_data1.jpg)

The dataset requires K clusters; however, trial and error are used to determine the optimal number of clusters, but for the purpose of practice, 3 clusters is optimal number for this dataset. Then, the DataFrame is fit into the K-means model and used to predict the clusters as ```class```. Lastly, visual plots with plotly and hvplot modules are utilized for clustering means. Another method for visualizing the clusters is plotly 3d model. 

![3dplot](unsuperised_pracitice_notebooks\img\plot3d.png)

After some trial and error, the elbow curve determines the optimal number of K clusters by measuring the amount of variation in the dataset. For this dataset, ```K=3``` was the optimal number of clusters. 

![elbow1](unsuperised_pracitice_notebooks\img\elbow_curve.png)

Lastly, to optimize machine learning, PCA (Principal Component Analysis) is utilized to maintain feature dimensionality and avoiding overfitting models. The use of transformation scalars to reduce features results in main ```K-n``` components that contain most of the information in the original dataset, with the components each having a certain ratio of variance of the dataset, although not 100% complete information is contained from the original.

A dendrogram graph is a similar feature to the elbow curve which helps determine the ideal number of clusters by keeping values of points on the x-axis, then connects all the points as they are clustered. An analyst could determine the ideal K clusters, depending on the range of their refined analysis. Starting from ```Y=0```, the higher a horizontal line, the less similarity there is between clusters. This method best fits the hierarchical clustering algorithm.

![dendo](unsuperised_pracitice_notebooks\img\dendogram1.jpg)

There are a few points to consider when comparing both K-mean and hierarchical clustering algorithms. K-means is dependent on random initialization, so the outcome depends on a random seed. An analyst might already consider K clusters prior to performing analysis. Utilizing dendrograms with hierarchical clustering, an analyst could pick an optimal number of clusters.



---



## Challenge
Use unsupervised learning to analyze data on the cryptocurrencies traded on the market.
