Article: Robust Single Image Super-Resolution via Deep Networks With Sparse Prior
tags: #manuscript 
backlinks:
Authors: Ding Liu, Zhaowen Wang, Bihan Wen, Jianchao Yang, Wei Han, Thomas S. Huang
Journal: IEEE Transactions on Image Processing
Date Published: 07/2016 
DOI: https://doi.org/10.1109/TIP.2016.2564643
URL: 

### Abstract:
Single image [[super-resolution]] (SR) is an ill-posed problem, which tries to recover a high-resolution image from its low-resolution observation. To regularize the solution of the problem, previous methods have focused on designing good priors for natural images, such as sparse representation, or directly learning the priors from a large data set with models, such as [[deep neural network]]s. In this paper, we argue that domain expertise from the conventional sparse coding model can be combined with the key ingredients of deep learning to achieve further improved results. We demonstrate that a sparse coding model particularly designed for SR can be incarnated as a neural network with the merit of end-to-end optimization over training data. The network has a cascaded structure, which boosts the SR performance for both fixed and incremental scaling factors. The proposed training and testing schemes can be extended for robust handling of images with additional degradation, such as noise and blurring. A subjective assessment is conducted and analyzed in order to thoroughly evaluate various SR techniques. Our proposed model is tested on a wide range of images, and it significantly outperforms the existing state-of-the-art methods for various scaling factors both quantitatively and perceptually.

#### Important Concepts:
Image super-resolution, [[deep neural networks]], [[sparse coding]], [[learned iterative soft thresholding algorithm (LISTA)]]


### Summary:
- This manuscripts proposes a model for single image super-resolution which capitalizes on the inherent sparsity found in natural images
- If defined properly with the right dictionaries $D_x,D_y$, both LR and HR have the same sparse vector
- Model uses LISTA to get this sparse code and trains a [[convolutional neural network]] to get the [[dictionary]] values
- They were able to treat SCN as a modular process for the creation of a cascade (CSCN) to get resolutions > 2x
- Through prior knowledge they were able to cut down on training time by reducing the number of parameters


### Methods:
- Standard CNN is improved by inclusion of [[learned iterative soft thresholding algorithm (LISTA)]] network: (Picture of LISTA and Figure 2)
- LISTA is able to be broken down into linear layers with neuronal layer with activation function
- 2D images which have undergone [[bicubic interpolation]] are used as inputs
- They shorcut initial feature extraction of the raw image (5x5 kernel, 100 features) by having 4 (5x5) filters be shifted to 25 positions
- They also use filters similar to the [[Haar filter]]s for these 4 filters
- Knowledge about ISTA is then used to create intelligent initial filter values
- [[subgradient descent]] is used with a [[mean squared error]] loss metric
- They also created cascade versions of models (CSCN)
- [[Peak signal-to-noise ratio (PSNR)]] and [[structural similarity index measure]] were the main metrics used to compare the SCN model


### Results:
- Improved performance for the following tasks:
	- 
- Compared against the following models:
	- 

### Discussion:
- Decent introduction to super-resolution
- Why only have 1 iteration of LISTA? Doesn't that imply it isn't important
- Good point that the loss in resolution between LR and HR is practically linear
- Also interesting the idea that LR and HR have the same sparse vector