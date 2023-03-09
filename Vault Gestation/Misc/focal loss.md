name : focal loss
tags : 
backlinks : 
source : https://medium.com/visionwizard/understanding-focal-loss-a-quick-read-b914422913e7
https://paperswithcode.com/method/focal-loss#:~:text=Focal%20loss%20applies%20a%20modulating,in%20the%20correct%20class%20increases.
https://www.analyticsvidhya.com/blog/2020/08/a-beginners-guide-to-focal-loss-in-object-detection/

###### Content:
An improved version of [[cross-entropy loss]] which accounts for [[class imbalance]] during training in tasks like [[object detection]] by assigning more weight to harder/easily misclassified examples (i.e. background with noisy texture, partial object, object of our interest, etc.) and to down-weight easy examples (i.e. background objects).

Formally, the focal loss adds a factor $(1-p_t)^\gamma$ to the standard [[cross-entropy loss]] criterion. Setting $\gamma >0$ reduces the relative loss for well-classified examples ($p_t > 0.5$), putting more focus on hard, misclassified examples. Here there is a tunable focusing parameter $\gamma \geq 0$. The equation for focal loss for $n$ categories is:

$$FL = -\sum_{i=1}^{n}(1-p_i)^\gamma log(p_i)$$
Where $p_i$ is the predicted probability of the example being the correct category (i.e. the probability output associated with the correct category: see [[cross-entropy loss]]). 

When a given example is misclassified, the $p_i$ is small, making $(1-p_t)^\gamma$ near $1$ and the loss unaffected. However, as the example becomes well classified and $p_i \rightarrow 1$, the $(1-p_t)^\gamma$ goes to zero, making the loss from this example down weighted. Thus, misclassified examples are given more weight in terms of loss calculation.

![[Pasted image 20230103145702.png]]
*Figure 1: Focal loss vs. [[cross-entropy loss]] with respect to the predicted classification of a single example of class $t$.*

###### Properties:
- In practice, you can use an $\alpha$-balanced variant of focal loss that borrows from [[balanced cross-entropy loss]], yielding slightly better accuracy than the non-balanced form $$FL = -\sum_{i=1}^n \alpha_i (i-p_i)^\gamma log(p_i)$$ where $\alpha_i$ is the weighting factor for class $i$.

###### Additional Thoughts:
