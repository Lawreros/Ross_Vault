name : boosting (hypothesis boosting)
tags : 
backlinks : 
source : #HOML , https://en.wikipedia.org/wiki/Boosting_(machine_learning)

###### Content:
Boosting (originally called hypothesis boosting) refers to any [[ensemble learning]] method that can combine several weak learners into a strong learner. The general idea of most boosting methods is to train predictors sequentially, each trying to correct its predecessor.

While boosting is not algorithmically constrained, most boosting algorithms consist of iteratively learning weak classifiers with respect to a distribution and adding them to a final strong classifier. When they are added, they are weighted in a way that is related to the weak learners' accuracy. After a weak learner is added, the data weights are readjusted, known as re-weighting, with misclassified input data gaining a higher wieght and properly classified input losing weight. Thus, future weak learners focus more on the examples that previous weak learners misclassified.

![[Pasted image 20220722120037.png]]

There are many boosting method available:
- [[AdaBoost]]
- [[Gradient Boosting]]
- [[Extreme Gradient Boosting]]

###### Properties:
- One disadvantage of boosting is that it is sensitive to outliers since every classifier is obliged to fix the errors in the predecessors. Thus, the method is too dependent on outliers.
- Another disadvantage is the method is almost impossible to scale up. This is due to every [[estimator]] basing its correctness on the previous predictions, thus making the procedure difficult to streamline.
- Boosting can be used with [[regression tree]]s. During boosting, a sequence of trees are trained and successive trees are cultivated on the residuals of preceding trees.

###### Additional Thoughts:
