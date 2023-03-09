name : U-Net
tags : 
backlinks : 
source : https://theaisummer.com/unet-architectures/, https://en.wikipedia.org/wiki/U-Net

###### Content:
U-Net is a [[convolutional neural network]] which modifies and extends a [[fully convolutional network]]. It gets its name from the U-shaped architecture which consists of a specific [[encoder-decoder]] scheme where the [[encoder]] reduces the spatial dimension (height/width/depth) in every [[layer]] and increases the channels. The [[decoder]] then increases the spatial dimension while reducing the channels. In the end, the spatial dimensions are restored to make a prediction for each pixel in the input image.

**Example:**
![[Pasted image 20221119180453.png]]
*Figure 1: Example of a U-Net model. with a depth of 5 (note the difference in dimensions for the concatenating data)* 

In the example displayed in Figure 1:
- The encoder (left side) consists of the repeated application of two 3x3 convolutions. Each convolution is followed by a [[ReLU]] and [[batch normalization]], with a 2x2 [[max pooling]] operation applied to reduce the spatial dimensions. At each downsampling step, the number of feature channels is doubled, while the number of spatial dimensions is halved.
- The decoder (right side) consists of repeated upsampling of the feature map followed by a 2x2 [[transposed convolutional layer]], which halves the number of feature channels. There is also a concatenation with the corresponding feature map from the contracting (encoder) path, and usually a 3x3 convolutional (each followed by a ReLU). At the final layer, a 1x1 convolution is used to map the channels to the desired number of classes.

###### Properties:
- The [[tensor]] that is passed in the decoder is usually called the "bottleneck"

###### Additional Thoughts:
