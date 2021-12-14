# Multilayer Perceptron (MLP)

Multilayer perceptron (MLP) is a supplement of feed forward neural network. It consists of three types of layers—the input layer, hidden layer, and output layer. The input layer receives the input signal to be processed. The required task such as prediction and classification is performed by the output layer. An arbitrary number of hidden layers that are placed in between the input and output layer are the true computational engine of the MLP. Similar to a feed forward network in a MLP the data flows in the forward direction from input to output layer. The neurons in the MLP are trained with the back propagation learning algorithm. MLPs are designed to approximate any continuous function and can solve problems which are not linearly separable. The major use cases of MLP are pattern classification, recognition, prediction and approximation.

<img src="https://www.researchgate.net/profile/Ryan-Heartfield/publication/321341597/figure/fig5/AS:667675554480148@1536197665532/MLP-deep-learning-architecture.ppm" width="550"/>

### Layers and activation function

The MLP consists of three or more layers (an input and an output layer with one or more hidden layers) of nonlinearly-activating nodes. Since MLPs are fully connected, each node in one layer connects with a certain weight ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20w_%7Bij%7D%7D) to every node in the following layer. For each layer ![](https://latex.codecogs.com/svg.latex?l), it will have two phases. The preactivation phase consists of a weighted linear combination of postactivation values in the previous layer. The postactivation values consists of passing the preactivation value through a chosen activation function elementwise. In MLP, some neurons use a nonlinear activation function. The two historically common activation functions are described by:

![](https://latex.codecogs.com/svg.latex?y%28%5Cupsilon_i%29%20%3D%20tanh%28%5Cupsilon_i%29)

![](https://latex.codecogs.com/svg.latex?y%28%5Cupsilon_i%29%20%3D%20%5Cfrac%7B1%7D%7B1%20&plus;%20e%5E%7B-%5Cupsilon_i%7D%7D)

In recent developments of deep learning the rectifier linear unit (ReLU) is more frequently used as one of the possible ways to overcome the numerical problems related to the sigmoids. The plot above uses the ReLU.

### Learning

Learning occurs in the perceptron by changing connection weights after each piece of data is processed, based on the amount of error in the output compared to the expected result. This is an example of supervised learning, and is carried out through backpropagation, a generalization of the least mean squares algorithm in the linear perceptron.

We can represent the degree of error in an output node ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20j%7D) in the ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20n%7D)th data point (training example) by ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20e_%7Bj%7D%28n%29%3Dd_%7Bj%7D%28n%29-y_%7Bj%7D%28n%29%7D), where ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20d%7D) is the target value and ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20y%7D) is the value produced by the perceptron. The node weights can then be adjusted based on corrections that minimize the error in the entire output, given by ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%7B%5Cmathcal%20%7BE%7D%7D%28n%29%3D%7B%5Cfrac%20%7B1%7D%7B2%7D%7D%5Csum%20_%7Bj%7De_%7Bj%7D%5E%7B2%7D%28n%29%7D).

Using gradient descent, the change in each weight is ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%5CDelta%20w_%7Bji%7D%28n%29%20%3D%20-%5Ceta%20%7B%5Cfrac%20%7B%5Cpartial%20%7B%5Cmathcal%20%7BE%7D%7D%28n%29%7D%7B%5Cpartial%20v_%7Bj%7D%28n%29%7D%7Dy_%7Bi%7D%28n%29%7D), where ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20y_%7Bi%7D%7D) is the output of the previous neuron and ![](https://latex.codecogs.com/svg.latex?%7B%5Cdisplaystyle%20%5Ceta%7D) is the learning rate, which is selected to ensure that the weights quickly converge to a response, without oscillations.

### Mini Batch

Mini batch divides the training data records into groups of approximately equal size, then updates the synaptic weights after passing one group; that is, mini-batch training uses information from a group of records. Then the process recycles the data group if necessary. Mini-batch training offers a compromise between batch and online training, and it may be best for "medium-size" datasets. The procedure can automatically determine the number of training records per mini-batch, or you can specify an integer greater than 1 and less than or equal to the maximum number of cases to store in memory.

# Reference

S. Abirami, P. Chitra (2020). Multilayer Perceptron. Advances in Computers. https://www.sciencedirect.com/topics/computer-science/multilayer-perceptron

Training (Multilayer Perceptron). https://www.ibm.com/docs/en/spss-statistics/24.0.0?topic=perceptron-training-multilayer

Multilayer perceptron. Wikipedia. https://en.wikipedia.org/wiki/Multilayer_perceptron
