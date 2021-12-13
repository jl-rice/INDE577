# K-Nearest Neighbors (KNN) Algorithm

In machine learning, the k-nearest neighbors (KNN) algorithm is a supervised and non-parametric classification method used for both classificationa and regression, but it is more widely used for classification. It is considered a non-parametric method because it does not make any assumptions about the underlying data distribution.

![Image of knn1](https://miro.medium.com/max/600/0*OltO4Txr-D0lPWNL.png)


### The KNN algorithm:
1. In both cases, the input consists of the ![](https://latex.codecogs.com/svg.latex?k) closest training examples in a data set. Choose ![](https://latex.codecogs.com/svg.latex?k%20%5Cin%20Z%5E%7B&plus;%7D).
2. The output depends on whether KNN is used for classification or regression:
   - KNN classification: the intuition is that data with similar features should be close in splace. Thus, KNN classification involves classifying an unobserved new data point by a plurality vote of its ![](https://latex.codecogs.com/svg.latex?k) nearest annotated data points. Then, the new data point will be assigned to the class most common among its ![](https://latex.codecogs.com/svg.latex?k) nearest neighbors.
   - KNN regression: the output is the property value for the object. This value is the average of the values of ![](https://latex.codecogs.com/svg.latex?k) nearest neighbors. The formula is shown below:

![](https://latex.codecogs.com/svg.latex?d%28p%2C%20q%29%20%3D%20%5Csqrt%7B%28p_1%20-%20q_1%29%5E2%20&plus;%20%28p_2%20-%20q_2%29%5E2%7D)


### Drawbacks of KNN algorithm:
- Curse of dimensionality: we usually just consider a two dimentional space, but as the number of dimensions increases, the amount of freedom for feature vectors to move around increases significantly. Every point is far away from every point else.
- Computational expensive: we need to compute the distance between the object and every single data points around it, so KNN is not used on extremely large datasets.


### Things we need to pay special attention to:
- Choice of ![](https://latex.codecogs.com/svg.latex?k): for classificaiton, ![](https://latex.codecogs.com/svg.latex?k) should be odd.
- Measure of performance: use error.

![](https://latex.codecogs.com/svg.latex?E%20%3D%20%5Cfrac%7B1%7D%7BM%7D%5Csum_%7Bi%20%3D%201%7D%5E%7BM%7D%20%28y_i%20%5Cneq%20%5Ctilde%7By_i%7D%29).

# References

Joby, Amal. What is k-nearest neighbor? An ML algorithm to classify data. July, 2021. https://learn.g2.com/k-nearest-neighbor

K-nearest neighbors algorithm. Wikipedia. https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm
