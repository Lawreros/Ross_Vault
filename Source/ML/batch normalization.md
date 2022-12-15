name : batch normalization (BN)
tags : 
backlinks : 
source : https://scortex.io/batch-norm-folding-an-easy-way-to-improve-your-network-speed/
https://machinelearningmastery.com/batch-normalization-for-training-of-deep-neural-networks/, https://towardsdatascience.com/batch-normalization-in-3-levels-of-understanding-14c2da90a338

###### Content:
Batch normalization is a technique for training very [[deep neural network]]s that attempts to reduce internal [[covariate shift]] by standardizing the inputs to a layer for each mini-batch. It consists of normalizing the activation vectors from hidden layers using the first and the second statistical moments (mean and [[variance]]) of the current mini-batch.This has the effect of stabilizing the learning process and dramatically reducing the number of training epochs required to train deep networks.

- *While it is considered one of the most important advances in the field of deep learning, the rationale for why it works so well is not fully understood. In a very loose sense, it makes the derivative calculation and weight adjustment during [[back-propagation]] more stable to the variability of the inputs you feed the models and makes the derivatives of each layer less dependent on each other. Read the links above for more information.*
- (see [this paper](https://arxiv.org/abs/1805.11604) as to why this may not be true) 

***Batch normalization is computed differently during the training and the testing phase.***
**Training:**
At each hidden [[layer]], batch normalization transforms the output signal $Z^{(i)}$ of training example $i$ (i.e. image number $i$ in the mini-batch of images $n$) as follows:
$$(1)\text{ } \mu = \frac{1}{n}\sum_i^n Z^{(i)}$$
$$(2)\text{ } \sigma^2 = \frac{1}{n}\sum_i (Z^{(i)}-\mu)^2$$
$$(3)\text{ } Z^{(i)}_{norm} = \frac{Z^{(i)}-\mu}{\sqrt{\sigma^2 - \epsilon}}$$
$$(4)\text{ } \hat{Z}^{(i)} = \gamma *Z^{(i)}_norm + \beta$$
The BN layer first determines the mean $\mu$ and variance $\sigma^2$ of the activation values across the patch, using $(1)$ and $(2)$. It then normalized the activation vector $Z^{(i)}$ with $(3)$. That way, each filter's output follows a standard [[normal distribution]] across the batch ($\epsilon$ is a constant used for numerical stability). It finally calculates the layer's output $\hat Z^{(i)}$ by applying a linear transformation with two trainable parameters. $\gamma, \beta$

![[Pasted image 20221125180655.png]]
*Figure 1: Example of a 3-neuron hidden layer, with a mini-batch of size b. Each neuron follows a [[standard normal distribution]]*

![[Pasted image 20221210175642.png]]

**Testing:**
Unlike the training phase, we may not have a full batch to feed into the model during the evaluation phase. To tackle this issue, we compute (𝜇_pop , σ_pop), such as :

𝜇_pop : estimated mean of the studied population;
σ_pop : estimated standard-deviation of the studied population.

Those values are computed using all the (𝜇_batch , σ_batch) determined during training, and directly fed into equation (3) during evaluation (instead of calling (1) and (2)).

###### Properties:
- Batch normalization relies on batch first and second statistical moments (mean and variance) to normalize hidden layers activations. The output values are then strongly tied to the current batch statistics. Such transformation adds some noise, depending on the input examples used in the current batch. (i.e. make sure the data in your batch is varied enough)
- Adding BN [[layer]]s allows for the use of higher [[learning rate]]s without compromising convergence. Thus leading to faster and better convergence (where better means higher accuracy)
- BN is dependent on batch size, with statistically more accurate mean and variance resulting from a larger batch size. If this is an issue (either for resources or total sample size, alternatives like [[layer normalization]] and [[instance normalization]] are potential alternatives which have similar higher learning rate benefits)

###### Additional Thoughts:
