name : k-distance graph
tags : 
backlinks : [[k-nearest neighbors]]
source : https://medium.com/@tarammullin/dbscan-parameter-estimation-ff8330e3a3bd

###### Content:
The k-distance graph is used to analyze the distance between each data point and its $k$-th nearest neighbor (and only that neighbor). Looking at a graph organized from least to most distance between a given point and its $k$ closest neighbor can give insight into the data (and hyperparameter selection for things like [[DBSCAN clustering]]).

**Example**
For each point in a dataset, the distance to its nearest neighbor is calculated and then the points are sorted from smallest to largest distance (epsilon):
![[Pasted image 20220504140409.png]]
for [[DBSCAN clustering]], the epsilon associated with the point of maximum curvature ($\epsilon = 30$) is a good starting value for the $\epsilon$ hyperparameter.

###### Properties:


###### Additional Thoughts:
