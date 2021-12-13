# Logistic Regression

Logistic Regression is a supervised machine learning algorithm that is used for the classification problems and predictive analysis. However, unlike the classification algorithm, logistic regression is strictly based on the concept of probability, and it is usually used to classify binary objects.

<img src="https://miro.medium.com/max/1400/1*dm6ZaX5fuSmuVvM4Ds-vcg.jpeg" width="630"/>

#### Comparison with linear regression:
We can call a logstic regression an extreme case of linear regression, but there are some clear differences between two. First, the predicted ![](https://latex.codecogs.com/svg.latex?y) of a logistic regression lies within 0 and 1, whereas a linear regression can have a predicted ![](https://latex.codecogs.com/svg.latex?y) exceedong this range. Also, the linear regression does not produce a probability, while a logistic regression does. In addition, the logistic regression uses a more complex cost function. This cost function can be defined as the "sigmoid function" or also known as the "logistic function" instead of a linear function.

![](https://latex.codecogs.com/svg.latex?Sigmoid%3A%20%5Csigma%28z%29%20%3D%20%5Cfrac%7B1%7D%7B1%20&plus;%20e%5E%7B-z%7D%7D)

![](https://latex.codecogs.com/svg.latex?Preactivation%3A%20z%20%3D%20%5Csum%20w_j%20x_j%20&plus;%20bias)

Below is a graph of the sigmoid function:

<img src="https://miro.medium.com/max/1280/1*OUOB_YF41M-O4GgZH_F2rw.png" width="500"/>

#### There are some general assumptions of the logistic regression:
1. Each example ![](https://latex.codecogs.com/svg.latex?%28x%2C%20y%29) belongs to one of two complementary classes.
2. Each example is independent of each other.
3. We assume all examples are generated under the same distribution.
4. The probability of "given ![](https://latex.codecogs.com/svg.latex?x) and predict the correct ![](https://latex.codecogs.com/svg.latex?y)", ![](https://latex.codecogs.com/svg.latex?p%28y%7Cx%29), is ![](https://latex.codecogs.com/svg.latex?%5Chat%7By%7D) if ![](https://latex.codecogs.com/svg.latex?y%20%3D%201), and ![](https://latex.codecogs.com/svg.latex?p%28y%7Cx%29) is ![](https://latex.codecogs.com/svg.latex?1%20-%20%5Chat%7By%7D) if ![](https://latex.codecogs.com/svg.latex?y%20%3D%200). We want to maximize ![](https://latex.codecogs.com/svg.latex?%5Chat%7By%7D) when ![](https://latex.codecogs.com/svg.latex?y%20%3D%201) and maximize ![](https://latex.codecogs.com/svg.latex?1%20-%20%5Chat%7By%7D) when ![](https://latex.codecogs.com/svg.latex?y%20%3D%200).

#### Derivations and outcomes:
We assume a bernoulli distribution for ![](https://latex.codecogs.com/svg.latex?p%28y%7Cx%29). Then, ![](https://latex.codecogs.com/svg.latex?p%28y%7Cx%29%20%3D%20%5Chat%7By%7D%5Ey%281%20-%20%5Chat%7By%7D%29%5E%7B1-y%7D). We want to maximize ![](https://latex.codecogs.com/svg.latex?p%28y%7Cx%29) by maximizing ![](https://latex.codecogs.com/svg.latex?log%28p%28y%7Cx%29%29), which is equivalent to minimizing ![](https://latex.codecogs.com/svg.latex?-log%28p%28y%7Cx%29%29), also known as the cross entropy loss (CEL). The loss function is important to implement the algorithm.

![](https://latex.codecogs.com/svg.latex?CEL%20%3D%20L%28w%2C%20b%3B%20y%29%20%3D%20-log%28p%28y%7Cx%29%29%20%3D%20-ylog%5Chat%7By%7D%20-%20%281-y%29log%281-%5Chat%7By%7D%29)

Then through partial derivatives, we finally obtain:

![](https://latex.codecogs.com/svg.latex?%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20w_j%7D%20%3D%20%5B%5Csigma%28w_j%20x_j%20&plus;%20bias%29%20%u2212%20y%5Dx_j%20%3D%20%5B%5Chat%7By%7D%20-%20y%5Dx_j)

![](https://latex.codecogs.com/svg.latex?%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20b%7D%20%3D%20%5Csigma%28w_j%20x_j%20&plus;%20bias%29%20-%20y%20%3D%20%5Chat%7By%7D%20-%20y)

#### Steps to train our neural network:
1. Randomly select ![](https://latex.codecogs.com/svg.latex?%28x%2C%20y%29) from the training set.
2. Feed forward into the neural network.
3. Use gradient descent to update weights and bias (choose the learning rate ![](https://latex.codecogs.com/svg.latex?%5Calpha)):
   - ![](https://latex.codecogs.com/svg.latex?w_1%20%3D%20w_1%20-%20%5Calpha%28%5Chat%7By%7D%20-%20y%29x_1)
   - ![](https://latex.codecogs.com/svg.latex?w_2%20%3D%20w_2%20-%20%5Calpha%28%5Chat%7By%7D%20-%20y%29x_2)
   - ...
   - ![](https://latex.codecogs.com/svg.latex?b%20%3D%20b%20-%20%5Calpha%28%5Chat%7By%7D%20-%20y%29)
4. Repeat step 1 to step 3 until desired loss in-sample is reached, or the maximum number of steps is reached.

# References

Logistic regression. Wikipedia. https://en.wikipedia.org/wiki/Logistic_regression

Pant, Ayush. Introduction to logistic regression. Jan 2019. https://towardsdatascience.com/
