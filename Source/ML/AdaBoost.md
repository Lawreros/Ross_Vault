name : AdaBoost
tags : 
backlinks : [[boosting]]
source : #HOML 

###### Content:
A type of [[boosting]] method for [[ensemble learning]] that works by training a series of predictors to fix the errors from a previous predictor. In order to build an AdaBoost classifier, a first base classifier (such as a [[decision tree]]) is trained and used to make predictions on the training set of data. The relative weight of the misclassified training data is then increased. A second classifier is trained using the updated weights and again it makes predictions on the training set, weights are updated, and so on:

![[Pasted image 20220722120954.png]]
*Figure: Decision boundaries of five consecutive predictors on a dataset. Each predictor is a highly regularized [[nonlinear SVM]] classifier*

In the figure, the first classifier gets may instances wrong, so their weights are boosted. The second classifier therefore does a better job on these instances, and so on.
To make predictions, AdaBoost simply computes the predictions of all the predictors and weighs them using the predictor weights. The predicted class is the one that receives the majority of weighted votes. (*For specific calculations/equations, see HOML pg. 203 on boosting*)

###### Properties:


###### Additional Thoughts:
