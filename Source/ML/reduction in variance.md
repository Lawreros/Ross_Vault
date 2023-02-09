name : reduction in variance
tags : 
backlinks : 
source : https://www.analyticsvidhya.com/blog/2020/06/4-ways-split-decision-tree/#:~:text=A%20decision%20tree%20makes%20decisions,concept%20that%20everyone%20should%20know.

###### Content:
Reduction in variance is a method for splitting the node of a [[decision tree]] when the target variable is continuous (i.e. a [[regression tree]]). It is called this because it uses [[variance]]s of the data points in each child node as a measure for deciding which feature to use when splitting. For each feature available to split across, the variance of the data inside of each child node is calculated:
$$Variance_{child} = \frac{\sum_{i=1}^{child}(x_i - \mu_{child})^2}{n_{child}}$$
A weighted average is then taken of all the child nodes and the feature which results in the lowest average variance is the one used for splitting.

###### Properties:


###### Additional Thoughts:
