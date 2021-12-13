# Decision Tree

A decision tree is a type of non-parametric supervised machine learning used to categorize or make predictions based on how a previous set of questions were answered. The model is defined by a series of questions that lead to a class label or a value when applied to any observation. Once set up, the model acts like a protocol in a series of “if this occurs then this occurs” conditions that produce a specific result from the input data.

### Terminology of decision tree
* Root node: the base of the decision tree.
* Splitting: the process of dividing a node into multiple sub-nodes.
* Decision node: when a sub-node is further split into additional sub-nodes.
* Leaf node: when a sub-node does not further split into additional sub-nodes; represents possible outcomes.
* Pruning: the process of removing sub-nodes of a decision tree.
* Branch: a subsection of the decision tree consisting of multiple nodes.

<img src="https://www.mastersindatascience.org/wp-content/uploads/tree-graphic.jpg" width="650" height="400"/>

Building a decision tree involves construction, in which you select the attributes and conditions that will produce the tree. Then, the tree is pruned to remove irrelevant branches that could inhibit accuracy. Pruning involves spotting outliers, data points far outside the norm, that could throw off the calculations by giving too much weight to rare occurrences in the data.

### Purity and impurity
A pure node contains only samples of the same class. In order to optimize our model we need to reach maximum purity and avoid impurity. To measure this we use the Gini impurity, which measures how often a randomly chosen element is labeled incorrectly if it was randomly labeled according to distribution. It is calculated by adding the probability, $p_i$, of an item with the label, $i$, being chosen multiplied by the times the probability $(1–p_i)$ of a mistake categorizing the time.

![](https://latex.codecogs.com/svg.latex?Gini%20%3D%201%20-%20%5Csum_%7Bi%20%3D%201%7D%5E%7Bc%7D%20p_i%5E2)

Our goal is to have it reach 0 where it will be minimally impure and maximally pure falling into one category.

# References

Accuracy, precision, recall & F1 score: interpretation of performance measures. 2016. https://blog.exsilio.com/all/accuracy-precision-recall-f1-score-interpretation-of-performance-measures/

What is a decision tree? https://www.mastersindatascience.org/learning/introduction-to-machine-learning-algorithms/decision-tree/
