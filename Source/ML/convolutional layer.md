name : convolutional layer
tags : 
backlinks : 
source : https://machinelearningmastery.com/convolutional-layers-for-deep-learning-neural-networks/, https://towardsdatascience.com/intuitively-understanding-convolutions-for-deep-learning-1f6f42faee1

###### Content:
Central to the [[convolutional neural network]] is the convolutional layer that gives the network its name. This [[layer]] performs an operation called a “_convolution_“.

In the context of a convolutional neural network, a convolution is a linear operation that involves the multiplication of a set of weights with the input, much like a traditional neural network. Given that the technique was designed for two-dimensional input, the multiplication is performed between an array of input data and a two-dimensional array of weights, called a [[filter]] or a kernel (*but it can be extended to N-dimensional inputs*).

The [[filter]] is smaller than the input data and the type of multiplication applied between a [[filter]]-sized patch of the input and the [[filter]] is a [[dot product]]. Because it results in a single value, the operation is often referred to as the “_scalar product_“.

Using a [[filter]] smaller than the input is intentional as it allows the same [[filter]] (set of weights) to be multiplied by the input array multiple times at different points on the input. Specifically, the [[filter]] is applied systematically to each overlapping part or [[filter]]-sized patch of the input data, left to right, top to bottom.

![[Pasted image 20221215142806.png]]
*Figure 1: 3x3 convolutional [[filter]] applied to a 6x6 image with padding of 1*

This systematic application of the same [[filter]] across an image is a powerful idea. If the [[filter]] is designed to detect a specific type of feature in the input, then the application of that [[filter]] systematically across the entire input image allows the [[filter]] an opportunity to discover that feature anywhere in the image. This capability is commonly referred to as *translation invariance*, e.g. the general interest in whether the feature is present rather than where it was present.

###### Properties:


###### Additional Thoughts:
