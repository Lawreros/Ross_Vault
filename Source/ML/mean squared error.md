name : mean squared error (MSE)
tags : 
backlinks : 
source : 

###### Content:
The MSE of an estimator (of a procedure for estimating an unobserved quantity) measures the average of the squares of the errors.

Let $\hat{Y}\in \mathbb{F}^n$ be the vector of predicted values generated from a sample of $n$ data points, and let $Y\in \mathbb{F}^n$ be the "true" observed values for said data points. The MSE can be calculated as:
$$MSE = \frac{1}{n} \sum_{i=1}^n (Y_i-\hat{Y_i})^2$$
Using matrix notation, where $e$ is a $n \times 1$ matrix and  $e_i = (Y_i - \hat{Y_i})$
$$MSE = \frac{1}{n} \sum_{i=1}^n (e_i)^2 = \frac{1}{n}e^Te$$

###### Properties:


###### Additional Thoughts:
