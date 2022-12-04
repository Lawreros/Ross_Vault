name : transposed convolutional layer
tags : 
backlinks : 
source : https://towardsdatascience.com/what-is-transposed-convolutional-layer-40e5e6e31c11#:~:text=Transposed%20convolutions%20are%20standard%20convolutions,in%20a%20standard%20convolution%20operation, https://d2l.ai/chapter_computer-vision/transposed-conv.html
https://medium.com/@marsxiang/convolutions-transposed-and-deconvolution-6430c358a5b6

###### Content:
A transposed convolutional [[layer]], unlike the [[convolutional layer]], is carried out for upsampling (i.e. to generate an output feature mat that has a spatial dimension greater than that of the input feature map). It does this by taking a given input and:
1. Inserting $d$ zeros between each row and column (commonly called the "dilation" value)
2. Applying a padding of $p$ around the perimeter of the input
3. Applying a convolution to the result using a **trainable** kernel. 
This allows you to take an input of size $n$-by-$m$ and get an output of $x$-by-$y$ (where $x \geq n$ and $m\geq y$) which interpolates some information about the newly created input values.


![[Pasted image 20221203183746.png]]
*Figure 1: Example of a 3x3 input with a dilation of 1 and a padding of 1. A 3x3 convolutional kernel is then applied, resulting in an upscaled 5x5 output.*


###### Properties:
- Wrongfully called a [[deconvolutional layer]], the difference being a deconvolution is a mathematical process that returns the original input before it was convoluted (think of the deconvolution being the inverse of a convolution, like with an [[invertible matrix]]). A transposed convolution does not perfectly recreate the original input.
- A transposed convolution is sometimes called a "fractionally-strided convolution"
- PyTorch's implementation of this is called `ConvTranspose2d`: https://pytorch.org/docs/stable/generated/torch.nn.ConvTranspose2d.html

###### Additional Thoughts:
