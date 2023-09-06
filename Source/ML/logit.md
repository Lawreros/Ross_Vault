name : logit
tags : 
backlinks : 
source : https://datascience.stackexchange.com/questions/31041/what-does-logits-in-machine-learning-mean, https://en.wikipedia.org/wiki/Logit

###### Content:
In terms of ML, logits can be interpreted to be unnormalized predictions of a model. Effectively, it is the raw output of a model before applying some form of normalization (like the [[softmax function]] for the outputs of a [[classification model]] to get the probability of each category). Another example would be the output of a [[segmentation model]], where each pixel of the output prediction corresponded to the probability it belonged to a given class.
*Read datascience.stackexchange.com link for good description*

Mathematically, the logit is the inverse of the standard logistic function (or [[softmax function]]):$$\sigma(x) = \frac{1}{1+e^{-x}}$$ so that the logit is defined as: $$logit(p) = \sigma^{-1}(p) = ln(\frac{p}{1-p})$$ for $p \in (0,1)$

###### Properties:


###### Additional Thoughts:
