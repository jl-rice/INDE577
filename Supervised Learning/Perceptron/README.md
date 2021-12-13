# Perceptron

In machine learning, perceptron is a single layer neural network. It is an algorithm for supervised learning of binary classifiers. A binary classifier is a function which can decide whether or not an input, represented by a vector of numbers, belongs to some specific class. It is a type of linear classifier, which is a classification algorithm that makes its predictions based on a linear predictor function combining a set of weights with the feature vector. As we can see from the picture below, the line linearly seperates the two different classes.

<img src="https://miro.medium.com/max/1400/1*xsR57_PO8U7PB_ItLslLmA.png" width="450"/>

There are generally four parts to implement perceptron, including inputing ![](https://latex.codecogs.com/svg.latex?X) values and a constant 1, weights and bias, weighted sum, and finally an activation function. Weights shows the strength of the particular node. A bias value allows us to shift the activation function curve up or down. The algorithm is illustrated as below.

<img src="https://miro.medium.com/max/4800/1*n6sJ4yZQzwKL9wnF5wnVNg.png" width="620"/>

### Detailed steps to implement perceptron:
1. Define ![](https://latex.codecogs.com/svg.latex?%5Cbar%7BX%7D) to be a vector containing ![](https://latex.codecogs.com/svg.latex?x_1) through ![](https://latex.codecogs.com/svg.latex?x_n) and a constant 1.
3. Compute the weighted sum ![](https://latex.codecogs.com/svg.latex?%5Csum%20%3D%20w%5ET%20%5Cbar%7BX%7D) plus a bias term. The weights ![](https://latex.codecogs.com/svg.latex?w) are obtained through gradient descent.
3. Input the weighted sum to an activation function, and then the activation function will give the output ![](https://latex.codecogs.com/svg.latex?%5Chat%7By%7D%20%3D%20sign%28w%5ET%20%5Cbar%7BX%7D%29).

# References

Perceptron. Wikipedia. https://en.wikipedia.org/wiki/Perceptron

Sharma, Sagar. What the hell is perceptron? https://towardsdatascience.com/what-the-hell-is-perceptron-626217814f53
