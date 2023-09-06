name : instance normalization
tags : 
backlinks : 
source : https://wandb.ai/wandb_fc/Normalization-Series/reports/Instance-Normalization-in-PyTorch-With-Examples---VmlldzoxNDIyNTQx, https://www.baeldung.com/cs/instance-vs-batch-normalization#:~:text=Instance%20normalization%20is%20another%20term,operates%20on%20a%20single%20sample.

###### Content:
Similar to [[batch normalization]] and [[layer normalization]], instance normalization is a technique for training very [[deep neural network]]s that attempts to reduce internal [[covariate shift]] by standardizing the inputs to a layer for each mini-batch. It is similar to [[batch normalization]], but instead of making the neuron/[[filter]] output across all items in the mini-batch a [[standard normal distribution]], the neuron/[[filter]] outputs for each individual channel for each sample of the mini-batch is normalized.

For a given input The mean and [[standard deviation]] are calculated per dimension separately for each object in a mini-batch.
$$y = \frac{x-E[x]}{\sqrt{Var[x]+\epsilon}} *\gamma + \beta$$ where $\epsilon << 0.01$ for numerical stability, $x$ is the input, and with two (optionally) trainable parameter vectors $\gamma, \beta$ of size $C$ (standing for [[weight]](s), [[bias]], and $C$ = number of input channels)

Specifically, given a sample of shape `[N,C,H,W]`, instance normalization calculates a mean and [[variance]] of all the elements of shape `[H,W]` in each mini-batch.

![[Pasted image 20221210175642.png]]

###### Properties:
- Like the other normalization techniques, instance normalization has the effect of stabilizing the learning process and dramatically reducing the number of training epochs required to train deep networks.
- While instance normalization transforms a single training sample, [[batch normalization]] does that to the whole mini-batch of samples. This makes [[batch normalization]] dependent on the batch size in that, to obtain a statistically more accurate mean and variance, the batch size needs to be large.

###### Additional Thoughts:
