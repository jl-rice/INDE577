# Ensemble Learning and Random Forest

### Ensemble Model

A single algorithm may not make the perfect prediction for a given dataset. Machine learning algorithms have their limitations and producing a model with high accuracy is challenging. If we build and combine multiple models, the overall accuracy could get boosted. Ensemble models is a machine learning approach to combine multiple other models in the prediction process. Those models are referred to as base estimators. It is a solution to overcome the following technical challenges of building a single estimator:

* High variance: The model is very sensitive to the provided inputs to the learned features.
* Low accuracy: One model or one algorithm to fit the entire training data might not be good enough to meet expectations.
* Features noise and bias: The model relies heavily on one or a few features while making a prediction.

There are many ensemble learning algorithms, such as bagging, random forest, stacking, boosting and so on.

<img src="https://cdn.analyticsvidhya.com/wp-content/uploads/2018/05/Screenshot-from-2018-05-08-13-11-49-850x642.png" width="450" height="300"/>


### Random Forest
Random forests or random decision forests are an ensemble learning method for classification, regression and other tasks. It uses subset of training samples as well as subset of features to build multiple split trees. Multiple decision trees are built to fit each training set. The distribution of samples/features is typically implemented in a random mode.

<img src="https://www.tibco.com/sites/tibco/files/media_entity/2021-05/random-forest-diagram.svg" width="550" height="360"/>

### Bagging
Another esemble learning method is bagging. Bagging is based on a bootstrapping sampling technique. Bootstrapping creates multiple sets of the original training data with replacement. Replacement enables the duplication of sample instances in a set. Each subset has the same equal size and can be used to train models in parallel.

### Difference between random forest and bagging
The key difference between bagging and random forest is that in Random forests, only a subset of features are selected at random out of the total and the best split feature from the subset is used to split each node in a tree, unlike in bagging where all features are considered for splitting a node.
