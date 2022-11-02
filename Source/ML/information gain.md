name : information gain
tags : 
backlinks : 
source : https://www.section.io/engineering-education/entropy-information-gain-machine-learning/

###### Content:
Information gain can be defined as a measure of how much information a feature provides about a class. Information gain is a commonly used metric during the construction of a [[decision tree]] for determining what feature to use when splitting nodes. This is done by evaluating the information gain for each feature with respect to the target variable (the [[classification]]) and selecting the variable that maximizes the gain (which in turn minimizes [[entropy]]).

$$\text{Information Gain} = E_{parent} - E_{children}$$
Where $E_{parent}$ is the [[entropy]] of the parent node and $E_{children}$ is the (weighted by number of data points in each node) average entropy of the child nodes.

###### Properties:


###### Additional Thoughts:
