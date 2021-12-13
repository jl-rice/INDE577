# Gradient Descent

Gradient descent is a first-order iterative optimization machine learning algorithm used to minimize some function by iteratively moving in the direction of steepest descent as defined by the negative of the gradient. We use gradient descent to update the parameters of our model. Since gradient descent is commonly used to train machine learning models and neural networks, the parameters refer to coefficients in linear regression and weights in neural networks. 

<img src="http://rasbt.github.io/mlxtend/user_guide/general_concepts/gradient-optimization_files/ball.png" width="500"/>

#### Basic concepts of neural networks:
1. Weights and bias.
2. Activation function.
3. Loss function.

#### Steps to implement gradient descent in linear models:
1. We start with a linear model $\hat{y} = \hat{w_i}X + b$. Our goal is to find the optimal linear function approximating the data. Here, w and b are weight and bias respectively.
2. Define a loss function. A loss function tells us “how good” our model is at making predictions for a given set of parameters. The cost function has its own curve and its own gradients. The slope of this curve tells us how to update our parameters to make the model more accurate. The loss function is shown below, and M refers to the number of data points.

$$
L = \frac{1}{2M}\sum_{i = 1}^{M}(\hat{w_i}x_i + b - y_i)^2
$$

3. Use gradient descent to calculate the gradient of the loss function.
$$
\frac{\partial L}{\partial w} = \frac{1}{M}\sum_{i = 1}^{M}(\hat{w_i}x_i + b - y_i)x_i
$$

$$
\frac{\partial L}{\partial b} = \frac{1}{M}\sum_{i = 1}^{M}(\hat{w_i}x_i + b - y_i)
$$

4. Choose a learning rate $\alpha$. Also, select a max_iteration, and set count to 0.
5. While count is smaller than  max_iteration, we update $\hat{w} = \hat{w} - \alpha\frac{\partial L}{\partial w}$, and update $b = b - \alpha\frac{\partial L}{\partial b}$. Count increases by 1.

# References

Gradient descent. Wikipedia. https://en.wikipedia.org/wiki/Gradient_descent

Gradient descent. 2017. https://ml-cheatsheet.readthedocs.io/en/latest/gradient_descent.html#gradient-descent
