name : covariate shift (internal covariate shift)
tags : 
backlinks : 
source : https://www.seldon.io/what-is-covariate-shift, https://wiki.tum.de/display/lfdv/Batch+Normalization

*Note: covariate shift and internal covariate shift are slightly different, so read all the way through*
###### Content:
**Covariate Shift:**
Covariate shift in machine learning is a type of model drift which occurs when the distribution of [[independent]] variables changes between the training environment and the live environment. In [[supervised learning]] a model will learn the relationship between input and output data through training datasets in [[batch learning]]/offline environment. The model can then be used to make predictions or classify new data using the patterns it has learned. Covariate shift occurs when the distribution of variables in the training data is different to real-world or testing data. This means that the model may make the wrong predictions once it is deployed, and its accuracy will be significantly lower. Detecting and addressing covariate shift is therefore a key step to the machine learning process. 

Covariate shift is a common occurrence when deploying machine learning models. It happens when there is a difference in input distribution between the training data and live or test data, and this can happen for a number of reasons. For example, facial recognition models may have just been trained on the faces of people aged 20 to 30. When deployed, the model will naturally be less accurate when trying to map the faces of older people with different facial structures.  

**Internal Covariate Shift:**
When covariate shift happens on the input of internal [[layer]]s of [[deep neural network]]s, it is called an internal covariate shift.

In order to visualize the meaning of this, assume there exist two conditional distributions of data, the distribution of the source data $P_S(Y|X)$ and the distribution of the target data $P_t(Y|X)$, with  $P_S(Y|X)=Pt(Y|X)=P(Y|X)$, but $P_S(X) \neq Pt(X)$. This can also be viewed as the input data of two layers following one another. This alone would not lead to a problem, if $P(Y|X)$ would be used as the true data input for the network. The problem arises from the fact that everything related to sensors and computers involves a model $P(Y|X,\theta)$ of the data $P(Y|X)$, with $\theta$ being the parameters of the model.

For the same reason that [[back-propagation]], the specifics of the model parameters used are at best an approximation of the true data $P(Y|X)$, leading to a shift in the data distribution used, compared to the true distribution. In order to counteract this, re-training the network with a weighting of the data of the source by $\frac{P_t(X)}{P_S(X)}$, or similar technics, have to be applied.

In [[neural network]]s, this effect gets worse with a growing number of [[layer]]s, if no counter measurements are deployed. Since each output of a layer is the input of the next layer, the shift continues to grow. Even with the [[back-propagation]] and the subsequent change of $P_S(Y|X,\theta)$ and $Pt(Y|X,\theta'')$ to $Ps(Y|X,\theta''')$ and $Pt(Y|X,\theta'''')$, to better model the true data, the new parameters are based on the old, faulty data distribution, due to the aforementioned internal covariate shift. This effect can be minimal, if only a few layers are used, otherwise this has to be addressed through methods like [[batch normalization]] and [[layer normalization]].

###### Properties:
- Sometimes called "internal covariate shift" when dealing with the covariates inside of the model (i.e. the input to one layer from another layer)
- Covariate shift can be a sign that the model lacks the ability to generalize adequately.

###### Additional Thoughts:
