# K-Nearest Neighbors (KNN) Algorithm

In machine learning, the k-nearest neighbors (KNN) algorithm is a supervised and non-parametric classification method used for both classificationa and regression, but it is more widely used for classification. It is considered a non-parametric method because it does not make any assumptions about the underlying data distribution.

![Image of knn1](https://miro.medium.com/max/600/0*OltO4Txr-D0lPWNL.png)


### The KNN algorithm:
1. In both cases, the input consists of the k closest training examples in a data set. Choose $k \in Z^{+}$
2. The output depends on whether KNN is used for classification or regression:
   - KNN classification: the intuition is that data with similar features should be close in splace. Thus, KNN classification involves classifying an unobserved new data point by a plurality vote of its k nearest annotated data points. Then, the new data point will be assigned to the class most common among its k nearest neighbors.
   - KNN regression: the output is the property value for the object. This value is the average of the values of k nearest neighbors. The formula is shown below:

$$
d(p, q) = \sqrt{(p_1 - q_1)^2 + (p_2 - q_2)^2}
$$


### Drawbacks of KNN algorithm:
- Curse of dimensionality: we usually just consider a two dimentional space, but as the number of dimensions increases, the amount of freedom for feature vectors to move around increases significantly. Every point is far away from every point else.
- Computational expensive: we need to compute the distance between the object and every single data points around it, so KNN is not used on extremely large datasets.


### Things we need to pay special attention to:
- Choice of k: for classificaiton, k should be odd.
- Measure of performance: use error $E = \frac{1}{M}\sum_{i = 1}^{M} (y_i \neq \tilde{y_i})$.

# References

Joby, Amal. What is k-nearest neighbor? An ML algorithm to classify data. July, 2021. https://learn.g2.com/k-nearest-neighbor

K-nearest neighbors algorithm. Wikipedia. https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm
