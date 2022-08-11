name : entropy
tags : 
backlinks : 
source : https://www.javatpoint.com/entropy-in-machine-learning#:~:text=Introduction%20to%20Entropy%20in%20Machine,or%20impurity%20in%20the%20system.

###### Content:
Entropy is the measurement of disorder or impurities in the information processed in machine learning. Entropy is a useful tool in machine learning for understanding concepts like feature selection, building [[decision tree]]s, and fitting [[classification]] models.

Consider a data set of having a total number of $N$ classes, then the entropy $E$ can be determined with the formula: $$E = -\sum_{i=1}^N p_i log_2(p_i)$$
Where $p_i$ is the probability of randomly selecting an example in class $i$.

![[Pasted image 20220510132853.png]]
*Probability of selecting a "+" vs. entropy*

###### Properties:
- When entropy becomes 0, then the dataset has no impurity.
- Datasets with higher impurity are good for training, as they have a good ratio of different categories of data (i.e. you don't have 100 data points where 95 belong to category A, 2 belong to category B, and 3 belong to category C)
- With regards to [[decision tree]]s, when determining a split in a node, the more the decrease in entropy, the more [[information gain]].
- Used almost interchangeably with [[Gini impurity]], but has a slight disadvantage due to needing to calculate logarithmic values, which take slightly more time

###### Additional Thoughts:
