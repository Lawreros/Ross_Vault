Article: Robust Single Image Super-Resolution via Deep Networks With Sparse Prior
tags: #manuscript 
backlinks:
Authors: Ding Liu, Zhaowen Wang, Bihan Wen, Jianchao Yang, Wei Han, Thomas S. Huang
Journal: IEEE Transactions on Image Processing
Date Published: 07/2016 
DOI: https://doi.org/10.1109/TIP.2016.2564643
URL: 

### Abstract:
Single image [[super-resolution]] (SR) is an ill-posed problem, which tries to recover a high-resolution image from its low-resolution observation. To regularize the solution of the problem, previous methods have focused on designing good priors for natural images, such as sparse representation, or directly learning the priors from a large data set with models, such as [[deep neural network]]s. In this paper, we argue that domain expertise from the conventional sparse coding model can be combined with the key ingredients of deep learning to achieve further improved results. We demonstrate that a [[sparse coding]] model particularly designed for SR can be incarnated as a [[neural network]] with the merit of end-to-end optimization over training data. The network has a cascaded structure, which boosts the SR performance for both fixed and incremental scaling factors. The proposed training and testing schemes can be extended for robust handling of images with additional degradation, such as noise and blurring. A subjective assessment is conducted and analyzed in order to thoroughly evaluate various SR techniques. Our proposed model is tested on a wide range of images, and it significantly outperforms the existing state-of-the-art methods for various scaling factors both quantitatively and perceptually.

#### Important Concepts:
Image super-resolution, [[deep neural network]], [[sparse coding]], [[learned iterative soft thresholding algorithm (LISTA)]]

#### Data Type:
- 2D images, [[bicubic interpolation]]
- Datasets used:
	- [[Set91]]
	- [[BSD500]]
	- [[Set5]]
	- [[BSD100]]


### Summary:
This manuscript proposes a model for single image super resolution which capitalizes on the inherent sparsity of natural images. Generic [[convolutional neural network]]s and [[deconvolutional neural network]]s are designed such that they directly learn from training data in order to learn the non-linear mapping from low resolution (LR) space to high resolution (HR) space. This ignores people's domain expertise, such as:
- The assumption that the degradation from HR to LR is nearly linear. This means that,If defined properly, with the right dictionaries $D_x,D_y$, both LR and HR have the same [[sparse vector]]
- In the patch-based SR methods, natural image patches can be represented as the sparse linear combinations of [[dictionary]] [[atom]]s trained from external databases
Using this domain expertise, they propose the "sparse coding based network" (SCN) which achieves better SR performance with faster training (due to being able to calculate ideal initial model weights) and smaller model size.

The SCN model can only be trained to perform image SR by a particular scaling factor (x2, x3, ...), but they get around this by proposing a cascade of multiple SCNs (CSCN) in order to increase the scaling flexibility of their model.


### Methods:
- Take a patch from a given bicubic-upscaled LR image $y \in \mathbb{R}^{m_y}$ which has a corresponding patch in HR image, denoted as $x\in \mathbb{R}^{m_x}$
- It is assumed that the LR(HR) patch $y(x)$ can be represented with respect to an [[overcomplete dictionary]] $D_y(D_x)$ using some sparse linear coefficients $\alpha_y(\alpha_x)\in \mathbb{R}^n$
- Since the degradation process form $x$ to $y$ is nearly linear, the patch pair can share the same sparse code: $$\alpha_y = \alpha_x = \alpha$$ if the dictionaries $D_x$ and $D_y$ are defined properly.
- Therefore, for an input LR patch $Y$, the HR patch can be recovered as: $$x = D_x\alpha$$ such that $$\alpha = arg\text{ }\underset{z}{min}||y - D_yz||^2_2+\lambda||z||_1$$ where $||\cdot||_1$ is the [[L1 norm]] with is [[convex]] and sparsity inducing, and $\lambda$ is a [[regularization coefficient]].
- To learn the dictionary pair $(D_y,D_x)$, the loss function can be defined as: $$a$$
- In order to incorporate [[sparse coding]] into a neural network, a [[feed-forward neural network]] is proposed which efficiently approximates the sparse code $\alpha$ of the input signal $y$ as it would be obtained by solving for the given dictionary $D_y$. The network has a finite number of recurrent stages, each of which updates the intermediate sparse coding according to $$z_{k+1} = h_\theta(Wy+Sz_k)$$ where $h_\theta$ is an element-wise shrinkage function defined as $$[h_\theta(\alpha)]_i = sign(a_i)(|a_i|-\theta_i)_+$$ with positive thresholds $\theta$ and $[\alpha_1,\alpha_2,...,\alpha_n]=\alpha\in \mathbb{R}^n$. This is done through the use of the [[learned iterative soft thresholding algorithm (LISTA)]] to get a good approximation of the underlining sparse code.
  ![[Pasted image 20221105164251.png]]

  - The $k$ LISTA iterations are able to be broken down into two linear layers $W \in \mathbb{R}^{n\times m_y}$ and $S \in \mathbb{R}^{n\times n}$ and a non linear layer with [[activation function]] $h_\theta$. The activation function can be rewritten in order to restrict the number of tunable parameters into a combination of two linear scaling layers and a unit-threshold neuron: $$[h_\theta(\alpha)]_i = sign(a_i)(|a_i|-\theta_i)_+ = \theta_ih_1(a_i/\theta_i)$$
- The weights of the two scaling layers are [[diagonal matrix]]s defined by $\theta$ and its element-wise reciprocal respectively (see upper right of figure below). These linear layers can then be combined with the existing linear layers $W$, $S$, and $D_x$ due to them just being matrices which can be multiplied together (gray boxes in the figure below).
  ![[Pasted image 20221105154422.png]]

- To reduce the number of parameters, the authors of the paper implement a unique way of LR patch extraction (layer $H$). Instead of having a 100 2D convolution filters with weights to train, they instead have four 5x5 filters which are shifted to 25 fixed positions each, resulting in 100 unique filters.
  *For the sake of demonstrating this method, say we were using this method instead with a 2x2 filter $K$ and were shifting using 9 fixed positions in a 4x4 kernel. The resulting 9 filters used for convolution would look like:*
| k_1 | k_2 | 0   | 0   |
| --- | --- | --- | --- |
| k_3 | k_4 | 0   | 0   |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 0   |

| 0 | k_1 | k_2   | 0   |
| --- | --- | --- | --- |
| 0 | k_3 | k_4   | 0   |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 0   |
(6 more iterations)
| 0   | 0   | 0   | 0   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | k_1 | k_2 |
| 0   | 0   | k_3 | k_4 |
|     |     |     |     |
Where the values for $k_1,k_2, k_3,k_4$ are the same for each of the 9 kernels. If you were to do this for four different 2x2 filters ($K_1,K_2,K_3,K_4 \in M_4(\mathbb{R})$), you would have 36 unique filters. However, since you only have four 2x2 filters worth of weights to adjust (16 parameters total), the calculation requirement to training are greatly reduced ($36*9*9 = 2916$).
- They also use filters similar to the [[Haar filter]]s for these 4 filters
- Similarly, the patch combination layer $G$ is also split into these fixed layers which align the pixels in overlapping patches (effectively accounting for and undoing the process done in $H$) and applying a 1D convolutional layer for a weighted average of all overlapping pixels.
- The authors of the paper use the prior domain knowledge about sparsity and [[iterative soft thresholding algorithm (ISTA)]] in order to calculate the optimal starting weights to reduce training time.
$$w_1=C\cdot D_y^T$$$$w_2=I-D_y^TD_y$$$$w_3=(CL)^{-1}D_x$$
Where $w_1, w_2$ and $w_3$ denote the weights of the three subsequent layers after $H$ (in the gray boxes).
- [[subgradient descent]] is used with a [[mean squared error]] loss metric to fit the model
- [[Peak signal-to-noise ratio (PSNR)]] and [[structural similarity index measure]] were the main metrics used to compare the SCN model

- Below if the model for the CSCN, where they collect [[mean squared error]] after each upscaling using SCN in order to train all of the SCN models at the same time
![[Pasted image 20221105154503.png]]

- They also propose an iterative SR scheme that attempts to deal with blurry and noisy image upscaling by incorporating the [[block-matching and 3D filtering algorithm (BM3D)]]

### Results:
- The SCN model was compared against:
	- [[adjusted anchored neighborhood regression (A+)]]
	- [[convolutional neural network]]
- The SCN and CSCN models performed better then their competition for x2, x3, and x4 upscaling with respect to [[Peak signal-to-noise ratio (PSNR)]] and [[structural similarity index measure]]
- When compared to a CNN of similar parameter size, the SCN model was able to converge much faster and achieved similar performance with less than 1% of the back-propagation.

### Discussion:
- Decent introduction to super-resolution (plenty of different terminology to investigate)
- Why only have 1 iteration of LISTA? Doesn't that imply it isn't important
- Good point that the loss in resolution between LR and HR is practically linear
- Also interesting the idea that LR and HR have the same sparse vector