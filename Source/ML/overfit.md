name : overfit
tags : 
backlinks : 
source : https://machinelearningmastery.com/overfitting-and-underfitting-with-machine-learning-algorithms/

###### Content:
Overfitting refers to a model that models the training data too well. Overfitting happens when a model learns the detail and noise in the training data to the extent that it negatively impacts the performance of the model on new data. This means that the noise or random fluctuations in the training data is picked up and learned as concepts by the model.

###### Properties:
- Overfitting is more likely with nonparametric and nonlinear models that have more flexibility when learning a target function. As such, many nonparametric machine learning algorithms also include parameters or techniques to limit and constrain how much detail the model learns. For example, [[decision tree]]s are nonparametric algorithms that are very flexible and is subject to overfitting training data. This problem can be addressed by pruning a tree after it has learned in order to remove some of the detail it has picked up.

###### Additional Thoughts:
