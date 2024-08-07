name : Swish function
tags : 
backlinks : 
source : https://www.v7labs.com/blog/neural-networks-activation-functions#h1

###### Content:
An [[activation function]] which is based off of the [[sigmoid function]]
$$f(x) = x*sigmoid(x)$$

![[swish_function.png]]


###### Properties:
- Swish consistently matches or outperforms [[ReLU]] [[activation function]] on [[deep neural network]]s applied to various challenging domains such as [[image classification]]
- Swish is a smooth function that means that it does not abruptly change direction like ReLU does near $x=0$. Rather, it smoothly bends from 0 towards values < 0 and then upwards again.  
-  Small negative values were zeroed out in [[ReLU]] [[activation function]]. However, those negative values may still be relevant for capturing patterns underlying the data. Large negative values are zeroed out for reasons of sparsity making it a win-win situation.  
-  The swish function being non-monotonous enhances the expression of input data and weight to be learned.

###### Additional Thoughts:
