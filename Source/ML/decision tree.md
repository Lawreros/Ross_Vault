name : decision tree
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Decision_tree_learning, https://www.kdnuggets.com/2020/01/decision-tree-algorithm-explained.html

###### Content:
A decision tree is a non-parametric [[supervised learning]] method used for both [[regression]] and [[classification]] problems. The goal of using a decision tree is to create a training model that can be used to predict the class or value of the **target variable** by learning simple decision rules inferred from prior data. 

Decision trees used in machine learning fall into two categories:
- [[classification tree]]
- [[regression tree]]

A tree is created by taking a collection of labeled training data and using one or multiple algorithms to decide where and how to split a node into two or more sub-nodes in order to increase the purity of each node with respect to the target variable (the label for each data point). This process is repeated until some previously determined criteria is met (i.e. a maximum number of splits is performed, a minimum amount of purity is reached, etc.). These decision rules for splitting nodes can either be categorical or bounds, depending on the feature value.

![[Pasted image 20220510110649.png]]

The decision of which feature to use when splitting a node is very important and cannot be randomly done if you want good model accuracy. Common criteria devised by researchers for deciding which feature to use are:
- [[entropy]] minimization
- [[information gain]]
- [[Gini impurity]]
- [[reduction in variance]]
- [[chi-square statistic]]


###### Terminology:
- **Root Node:** Represents the entire population or sample and is further divided into two or more homogeneous sets.
- **Splitting:** The process of dividing a node into two or more sub-nodes
- **Decision Node:** When a sub-node splits into further sub-nodes, then it is called the decision node
- **Leaf/Terminal Node:** Nodes that do not split are called Leaf or Terminal nodes
- **Pruning:** When sub-nodes are removed from decision nodes. This can be thought of as the opposite of splitting.
- **Branch/Sub-Tree:** A subsection of the entire tree
- **Parent and Child Node:** A node that is divided into sub-nodes would be called the parent node, while the sub-nodes are called the child nodes

![[Pasted image 20220510104354.png]]

###### Properties:
- It is often better to set some maximum depth for a tree in order to prevent overfitting to data, especially if said data is higher dimension.

###### Additional Thoughts:
