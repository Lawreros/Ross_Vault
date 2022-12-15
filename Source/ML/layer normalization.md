name : layer normalization
tags : 
backlinks : 
source : https://scortex.io/batch-norm-folding-an-easy-way-to-improve-your-network-speed/, https://wandb.ai/wandb_fc/LayerNorm/reports/Layer-Normalization-in-Pytorch-With-Examples---VmlldzoxMjk5MTk1?galleryTag=beginner

###### Content:
A technique for training [[deep neural network]]s which hopes to address the issue of internal [[covariate shift]] (see [this paper](https://arxiv.org/abs/1805.11604) as to why this may not be true). It is similar to [[batch normalization]], but instead of making the filter output across all items in the mini-batch a [[standard normal distribution]], the filter outputs across all channels for each sample of the mini-batch is normalized.
Specifically, given a sample of shape `[N,C,H,W]`, layer normalization calculates a mean and [[variance]] of all the elements of shape `[C,H,W]` in each mini-batch and normalizes them.

![[Pasted image 20221210175642.png]]

###### Properties:
- Layer normalization has some benefits over [[batch normalization]], which quickly fails as soon as the number of batches are reduced. As modern day ML algorithms increase in data resolution, this becomes a big problem; the batch size needs to be small in order to fit data in memory. 
	- Batch normalization also requires the storing of the running mean and variance of [[activation function]]s at each [[layer]].
- Layer normalization only requires the calculation of mean and variances for individual items of a batch at a time, saving resources and allowing for [[online learning]]
- Like the other normalization techniques, layer normalization has the effect of stabilizing the learning process and dramatically reducing the number of training epochs required to train deep networks.

###### Additional Thoughts:
