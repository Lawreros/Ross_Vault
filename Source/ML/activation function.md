name : activation function
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Activation_function, https://www.v7labs.com/blog/neural-networks-activation-functions#h1

###### Content:
In [[neural network]]s, the activation function of a node defines the output of that node given an input or set of inputs.

![[Pasted image 20221119204430.png]]
*Figure 1: A node in a neural network receiving weighted inputs, summing them, and then applying an activation function $f$ to the sum. The output of the activation function determines the output value of the node.*

The purpose of an activation function is to add non-linearity to the neural network. *Let’s suppose we have a neural network working without the activation functions.  In that case, every neuron will only be performing a linear transformation on the inputs using the weights and biases. It’s because it doesn’t matter how many hidden layers we attach in the neural network; all layers will behave in the same way because the composition of two linear functions is a linear function itself. Although the neural network becomes simpler, learning any complex task is impossible, and our model would be just a linear regression model.*

###### Properties:
There are three types of neural network activation functions:
- **Binary Step Function:** The input fed to the activation function is compared to a certain threshold $a$; if the input is greater than it, then the neuron is activated, else it is deactivated, meaning the its output is not passed on to the next hidden layer. It can be represented as: $$f(x) = \begin{cases} 0& \text{for } x < a \\ 1& \text{for } x \geq a \end{cases}$$ Some limitations are:
	- It cannot provide multi-value outputs. For example, ti cannot be used for multi-class classification problems
	- The gradient of the step function is zero, causing hindrances in the back-propagation process.

- **Linear Activation Function:** The output of the function is the same as the input. $$f(x)=x$$
	Some limitations:
	- Back-propagation is not possible as the derivative of the function is a constant and has no relation to $x$
	- All layers of the neural network will collapse into one linear layer.

- **Non-Linear Activation Functions:** Activation functions which solve the following limitations of linear activation functions:
	-  They allow back-propagation because now the derivative function would be related to the input, and it’s possible to go back and understand which weights in the input neurons can provide a better prediction.
	- They allow the stacking of multiple layers of neurons as the output would now be a non-linear combination of input passed through multiple layers. Any output can be represented as a functional computation in a neural network.
	- [[sigmoid function]]
	- [[ReLU]]
	- [[Leaky ReLU]]
	- [[Softmax function]]
	- [[Swish function]]

###### Additional Thoughts:
