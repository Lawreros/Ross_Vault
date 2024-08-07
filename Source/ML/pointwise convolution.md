name : pointwise convolution
tags : 
backlinks : 
source : https://paperswithcode.com/method/pointwise-convolution, https://towardsdatascience.com/a-basic-introduction-to-separable-convolutions-b99ec3102728

###### Content:
Pointwise convolution is a type of convolution that uses a 1x1 kernel with depth equal to however many channels the input image has. The kernel iterates through every single point along the input image, multiplying each channel by a different scalar before summing the resulting values (though often some sort of [[activation layer]] is applied, such as [[ReLU]], [[PReLU]], [[softmax function]].

![[Pasted image 20221119194933.png]]
*Figure 1: Example of the application of a pointwise convolution to a 8x8 image with 3 channels.*

###### Properties:
- Multiple 1x1 kernels can be used in order to increase the number channels from a given input

###### Additional Thoughts:
- Read through the Towards Data Science source link for a good explanation of why pointwise convolutions are used:
	- *For me, however, the main purpose of a 1x1 kernel is to apply non-linearlity. After every layer of a neural network, we can apply an activation layer. Whether it be ReLU, [[PReLU]], Softmax, or another, activation layers are non-linear, unlike convolution layers. “A linear combination of lines is still a line.” Non-linear layers expand the possibilities for the model, as is what generally makes a “deep” network better than a “wide” network. In order to increase the number of non-linear layers without significantly increasing the number of parameters and computations, we can apply a 1x1 kernel and add an activation layer after it. This helps give the network an added layer of depth.*