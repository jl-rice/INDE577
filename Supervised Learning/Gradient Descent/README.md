# Gradient Descent

Gradient descent is a first-order iterative optimization machine learning algorithm used to minimize some function by iteratively moving in the direction of steepest descent as defined by the negative of the gradient. We use gradient descent to update the parameters of our model. Since gradient descent is commonly used to train machine learning models and neural networks, the parameters refer to coefficients in linear regression and weights in neural networks. 

<img src="http://rasbt.github.io/mlxtend/user_guide/general_concepts/gradient-optimization_files/ball.png" width="500"/>

### Basic concepts of neural networks:
1. Weights and bias.
2. Activation function.
3. Loss function.

### Steps to implement gradient descent in linear models:
1. We start with a linear model ![](https://latex.codecogs.com/svg.latex?%5Chat%7By%7D%20%3D%20%5Chat%7Bw_i%7DX%20&plus;%20b). Our goal is to find the optimal linear function approximating the data. Here, ![](https://latex.codecogs.com/svg.latex?w) and ![](https://latex.codecogs.com/svg.latex?b) are weight and bias respectively.
2. Define a loss function. A loss function tells us “how good” our model is at making predictions for a given set of parameters. The cost function has its own curve and its own gradients. The slope of this curve tells us how to update our parameters to make the model more accurate. The loss function is shown below, and M refers to the number of data points.

![First equation](https://latex.codecogs.com/svg.latex?L%20%3D%20%5Cfrac%7B1%7D%7B2M%7D%5Csum_%7Bi%20%3D%201%7D%5E%7BM%7D%28%5Chat%7Bw_i%7Dx_i%20&plus;%20b%20-%20y_i%29%5E2)

3. Use gradient descent to calculate the gradient of the loss function.

![](https://latex.codecogs.com/svg.latex?%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20w%7D%20%3D%20%5Cfrac%7B1%7D%7BM%7D%5Csum_%7Bi%20%3D%201%7D%5E%7BM%7D%28%5Chat%7Bw_i%7Dx_i%20&plus;%20b%20-%20y_i%29x_i)

![](https://latex.codecogs.com/svg.latex?%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20b%7D%20%3D%20%5Cfrac%7B1%7D%7BM%7D%5Csum_%7Bi%20%3D%201%7D%5E%7BM%7D%28%5Chat%7Bw_i%7Dx_i%20&plus;%20b%20-%20y_i%29)

4. Choose a learning rate ![](https://latex.codecogs.com/svg.latex?%5Calpha). Also, select a max_iteration, and set count to 0.
5. While count is smaller than  max_iteration, we update ![](https://latex.codecogs.com/svg.latex?%5Chat%7Bw%7D%20%3D%20%5Chat%7Bw%7D%20-%20%5Calpha%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20w%7D), and update ![](https://latex.codecogs.com/svg.latex?b%20%3D%20b%20-%20%5Calpha%5Cfrac%7B%5Cpartial%20L%7D%7B%5Cpartial%20b%7D). Count increases by 1.

# References

Gradient descent. Wikipedia. https://en.wikipedia.org/wiki/Gradient_descent

Gradient descent. 2017. https://ml-cheatsheet.readthedocs.io/en/latest/gradient_descent.html#gradient-descent
