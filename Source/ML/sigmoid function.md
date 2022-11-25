name : sigmoid function (logistic [[activation function]])
tags : 
backlinks :
source : 

###### Content:
A sigmoid function is a mathematical function which has a characteristic "S"-shaped curve or sigmoid curve. A common example of the sigmoid function is defined by the formula:
$$\sigma(x) = \frac{1}{1+e^{-x}}$$
where $x \in \mathbb{R}$. This function serves to take any input value $x$ and bound the output value between $0$ and $1$, with $\sigma(0) = 0.5$

![Logistic Regression](https://devopedia.org/images/article/305/5893.1610998124.png)

###### Properties:
-   It is commonly used for models where we have to predict the probability as an output. Since probability of anything exists only between the range of 0 and 1, sigmoid is the right choice because of its range.
-   The function is differentiable and provides a smooth gradient, i.e., preventing jumps in output values. This is represented by an S-shape of the sigmoid activation function.
- For values greater than 3 or less than -3, the function will have very small gradients. As the gradient value approaches zero, the network ceases to learn and suffers from the [[vanishing gradient]] problem  
- The output of the logistic function is not symmetric around zero. So the output of all the neurons will be of the same sign. This makes the training of the [[neural network]] more difficult and unstable.

###### Additional Thoughts:
