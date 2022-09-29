name : support vector machine (SVM)
tags : 
backlinks : 
source : #HOML , wikipedia

###### Content:
Support-vector machines are [[supervised learning]] models that analyze data for [[classification]] and [[regression]] analysis. SVMs view data points as $p$-dimensional vectors which belong to one of two classes and can be separated by a $(p-1)$-dimensional [[hyperplane]].  After the model is created using training data to find this hyperplane, it can then be used to classify new data by determining which side of the hyperplane it falls on.

As there are many hyperplane that might classify the data, the "best" hyperplane is chosen so that the distance fro it to the nearest data point on each side is maximized.

If the data points are easily [[linearly separable]], then only a [[linear SVM]] model is required to accurately classify. In addition to performing linear classification, SVMs can efficiently perform a non-linear classification using what is called the "[[kernel trick]]", implicitly mapping their inputs into higher-dimensional spaces (see [[nonlinear SVM]]).

*For calculations used to find the hyperplane for the SVM, see [[linear SVM]]*

###### Properties:
- Classification of images has been performed using SVMs. Experimental results show that SVMs achieve significantly higher search accuracy than traditional query refinement schemes after just three to four rounds of relevance feedback.
- Hand-written characters can be recognized using SVM

###### Additional Thoughts:
