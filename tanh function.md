name : tanh function (hyperbolic tangent)
tags : 
backlinks : [[activation function]]
source : https://www.v7labs.com/blog/neural-networks-activation-functions#h1

###### Content:
The tanh function is very similar to the [[sigmoid function]] (as it was made to address some of sigmoid's issues), and even has the same "S"-shape with the difference being an output range of -1 to 1. In tanh, the larger the input (more positive), the closer the output value will be to 1.0, whereas the smaller the input (more negative), the closer the output will be to -1.0.
![[Pasted image 20221121181924.png]]
$$f(x) = \frac{(e^x - e^{-x})}{(e^x+e^{-x})}$$

###### Properties:
- The output of the tanh activation function is zero centered; hence we can easily map the output values as strongly negative, neutral, or strongly positive.
- Usually used in hidden layers of a neural network as its values lie between -1 to 1; therefore, the mean for the hidden layer comes out to be 0 or very close to it. It helps in centering the data and makes learning for the next layer much easier.
- Although both [[sigmoid function]] and tanh face [[vanishing gradient]] issue, tanh is zero centered, and the gradients are not restricted to move in a certain direction. Therefore, in practice, tanh nonlinearity is always preferred to sigmoid nonlinearity.

###### Additional Thoughts:
