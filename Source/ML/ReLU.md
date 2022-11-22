name : Rectified Linear Unit (ReLU)
tags : 
backlinks : [[Leaky ReLU]]
source : https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook, https://www.v7labs.com/blog/neural-networks-activation-functions#h1

###### Content:
The ReLU is the most commonly used [[activation function]] in [[deep neural network]]s. The function returns 0 if it receives any negative input, but for any positive value $x$ it returns that value back. This can be written as: $$f(x) = max(0,x)$$
*Read [link](https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook) for why ReLU is so powerful*

###### Properties:
- Since only a certain number of neurons are activated, the ReLU function is far more computationally efficient when compared to the [[sigmoid function]] and [[tanh function]].
- ReLU accelerates the convergence of [[gradient descent]] towards the global minimum of the [[loss function]] due to its linear, non-saturating property.
- The negative side of the graph makes the gradient value zero. Due to this reason, during the [[back-propagation]] process, the weights and biases for some neurons are not updated. This can create dead neurons which never get activated.
	- All the negative input values become zero immediately, which decreases the model’s ability to fit or train from the data properly.


###### Additional Thoughts:
