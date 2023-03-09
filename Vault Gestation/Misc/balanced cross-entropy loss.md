name : balanced cross-entropy loss
tags : 
backlinks : 
source : https://towardsdatascience.com/focal-loss-a-better-alternative-for-cross-entropy-1d073d92d075
https://www.analyticsvidhya.com/blog/2020/08/a-beginners-guide-to-focal-loss-in-object-detection/

###### Content:
Balanced cross-entropy loss is the [[cross-entropy loss]] function adapted to account for [[class imbalance]] in a given training set. It does this by adding a weighting factor to each class used in the [[classification model]]. 

Say that your training set contains 200 examples of category A for every example of category B. The majority class examples will dominate the loss function and gradient descent, causing the weights to update in the direction of the model becoming more confident in predicting the majority class while putting less emphasis on the minority classes.

Balanced cross-entropy loss adds a weighting factor to each class, which is represented by $0 \leq \alpha \leq 1$. The $\alpha$ could be the inverse class frequency or a hyper-parameter that is determined by cross-validation. The alpha parameter replaces the actual label term ($Y_i$) in the [[cross-entropy loss]] equation, resulting in:
$$BCE = -\sum_{i=1}^n \alpha_i log(p_i)$$
where $p_i$ is the predicted probability of the example being categorized as $i$ and $log$ is the natural log.

###### Properties:
- Despite the fact that this loss function addresses the issue of class imbalance, it cannot distinguish between hard and easy examples. Easily classified negatives comprise the majority of the loss and dominate the gradient. While balances the importance of positive/negative examples, it does not differentiate between easy/hard examples. The problem is addressed by [[focal loss]].

###### Additional Thoughts:
