name : logistic [[regression]]
tags : 
backlinks : 
source : Deep Learning

###### Content:
An algorithm which takes in input feature vector $x \in \mathbb{R}^{n_x}$ and outputs a prediction $\hat{y}$ which represents the probability that $y=1$ given the input $x$. 
$$\hat{y} = P(y=1 | x)$$
$$\hat{y} = \sigma(w^T x +b)$$
Where $w \in \mathbb{R}^{n_x}$ are the weights attributed to each of the features of $x$, and $b \in \mathbb{R}$ is some constant (sometimes called the "intercept"), and $\sigma$ is the [[sigmoid function]].

###### Properties:


###### Additional Thoughts:
