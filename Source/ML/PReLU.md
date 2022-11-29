name : PReLU (Parameterized [[ReLU]])
tags : 
backlinks : 
source : https://paperswithcode.com/method/prelu#:~:text=A%20Parametric%20Rectified%20Linear%20Unit,a%20slope%20for%20negative%20values. https://medium.com/@shauryagoel/prelu-activation-e294bb21fefa

###### Content:
A Parametric Rectified Linear Unit, or PReLU, is an activation function that generalizes the traditional [[ReLU]] with a slope for negative values. Formally:
$$f(y_i) = y_i \text{ if } y_i\geq 0$$
$$f(y_i) = a_iy_i \text{ if } y_i\leq 0$$
Where $a_i$ is a scalar learned parameter either for a given layer $i$ or a given channel $i$ in a given layer (i.e. either a different $a$ for each layer or a different $a$ for each channel in each layer, see the pytorch documentation). The intuition is that different layers may require different types of nonlinearity.

###### Properties:


###### Additional Thoughts:
