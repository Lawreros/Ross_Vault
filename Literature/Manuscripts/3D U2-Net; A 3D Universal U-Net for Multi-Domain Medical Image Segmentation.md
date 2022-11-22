Article: 3D U2-Net; A 3D Universal U-Net for Multi-Domain Medical Image Segmentation
tags: #manuscript 
backlinks:
Authors: 
Journal: 
Date Published: 
DOI: 
URL: 

### Abstract:
[[fully convolutional network]]s like [[U-Net]] have been the state-of-the-art methods in medical [[image segmentation]]. Practically, a network is highly specialized and trained separately for each segmentation task. Instead of a collection of multiple models, it is highly desirable to learn a universal data representation for different tasks, ideally a single model with the addition of a minimal number of parameters steered to each task. Inspired by the recent success of [[multi-domain learning]] in image classification for the first time we explore a promising universal architecture that handles multiple medical segmentation tasks and is extendable for new tasks, regardless of different organs and imaging modalities. Our 3D Universal U-Net (3D $U^2$-Net) is build upon separable convolution, assuming that images from different domains have domain-specific spatial correlations which can be probed with channel-wise convolution while also share cross-channel correlations which can be modeled with [[pointwise convolution]]. We evaluate the 3D $U^2$-Net on five organ segmentation dataset. Experimental results show that this universal network is capable of competing with traditional models in terms of segmentation accuracy, while requiring only about $1\%$ of the parameters. Additionally, we observe that he architecture can be easily and effectively adapted to a new domain without sacrificing performance in the domains used to learn the shared parameterization of the universal network.

#### Important Concepts:
- [[Lovasz-Softmax loss]]


#### Data Type


### Summary:
- Good explanation of residual adapters: https://proceedings.neurips.cc/paper/2017/file/e7b24b112a44fdd9ee93bdf998c6ca0e-Paper.pdf
- https://towardsdatascience.com/a-basic-introduction-to-separable-convolutions-b99ec3102728

### Results:



### Discussion:
- A good explanation can be found at the bottom of this article: https://theaisummer.com/unet-architectures/