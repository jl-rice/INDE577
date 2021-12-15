# K-Means Clustering

### PCA

Principal component analysis (PCA) is used in exploratory data analysis and for making predictive models. It is commonly used for dimensionality reduction by projecting each data point onto only the first few principal components to obtain lower-dimensional data while preserving as much of the data's variation as possible. The first principal component can equivalently be defined as a direction that maximizes the variance of the projected data. The ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20i%7D)th principal component can be taken as a direction orthogonal to the first ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20i-1%7D) principal components that maximizes the variance of the projected data.

For this project, we will first use PCA to reduce a four dimensional dataset to a two dimensional dataset. Then the two remaining features will be used to implement the k-means clustering algorithm.

### K-Means Clustering
K-means clustering is one of the simplest and popular unsupervised machine learning algorithms. Typically, unsupervised algorithms make inferences from datasets using only input vectors without referring to known, or labelled, outcomes. To process the learning data, the K-means algorithm in data mining starts with a first group of randomly selected centroids, which are used as the beginning points for every cluster, and then performs iterative (repetitive) calculations to optimize the positions of the centroids. It halts creating and optimizing clusters when either the centroids have stabilized (there is no change in their values because the clustering has been successful) or the defined number of iterations has been achieved.

<img src="https://miro.medium.com/max/1400/0*irrlUXS1tmYanvT0.png" width="700"/>

### The complete k-means clustering algorithm:
1. Randomly choose ![](https://latex.codecogs.com/svg.latex?k) distinct feature vectors as the starting centroids, ![](https://latex.codecogs.com/svg.latex?c_1), ![](https://latex.codecogs.com/svg.latex?c_2), ..., ![](https://latex.codecogs.com/svg.latex?c_k).
2. Assign each feature vector to the closest centroid. Clusters are formed accordingly.

![](https://latex.codecogs.com/svg.latex?A_i%20%3D%20%5C%7Bx%3A%20x_i%5C%20is%5C%20assigned%5C%20c_i%5C%7D)

3. Update centroids using ![](https://latex.codecogs.com/svg.latex?c_i%20%5Crightarrow%20%5Cfrac%7B1%7D%7B%7CA_i%7C%7D%5Csum_%7Bx%20%5Cin%20A_i%7D%5E%7B%7D%20x).
4. Repeat step 2 and step 3 until the centroids no longer move.
5. Return ![](https://latex.codecogs.com/svg.latex?A_1), ![](https://latex.codecogs.com/svg.latex?A_2), ..., ![](https://latex.codecogs.com/svg.latex?A_k).

# References

Garbade, Michael. Understanding k-means clustering in machine learning. Toward Data Science. https://towardsdatascience.com/understanding-k-means-clustering-in-machine-learning-6a6e67336aa1

Principal component analysis. Wikipedia. https://en.wikipedia.org/wiki/Principal_component_analysis
