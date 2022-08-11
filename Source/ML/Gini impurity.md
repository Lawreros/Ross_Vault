name : Gini impurity (Gini index)
tags : 
backlinks : 
source : 

###### Content:

Consider a dataset $D$ that contains samples from $k$ classes. The probability of samples belonging to class $i$ at a given node can be denotes as $p_i$. The Gini impurity of $D$ is defined as:
$$Gini(D) = 1-\sum_{i=1}^k p_i^2$$
Where $p_i$ is the probability of randomly selecting an example in class $i$.

###### Properties:
- The **Gini gain** can be calculated similarly to the [[information gain]]: $$\Delta Gini(A) = Gini_{parent}(D)-Gini_{children}(D)$$ where $Gini_{children}$ is the (weighted by number of data points in each node) average entropy of the child nodes.
- The Gini impurity has values inside of the interval $[0, 0.5]$
- Used almost interchangeably with [[entropy]], but has a slight advantage due to not needing to calculate logarithmic values, which take slightly more time

###### Additional Thoughts:
