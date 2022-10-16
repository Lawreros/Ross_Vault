name : Gradient Boosting
tags : 
backlinks : 
source : #HOML 

###### Content:
A popular [[boosting]] algorithm, similar to [[AdaBoost]], which works by sequentially adding predictors to an [[ensemble learning]] setup where each predictor is correcting its predecessor. However, instead of tweaking the instance weights at each iteration like [[AdaBoost]], this method tries to fit the new predictor to the residual errors made by the previous predictor.

![[Pasted image 20220722124349.png]]
*Figure: The predictions of three sequential [[regression tree]]s in the left column, and the ensemble's predictions in the right column. In the first row, the ensemble has just one tree, so its predictions are exactly the same as the first tree's predictions. In the second row, a new tree is trained on the residual errors of the first tree. On the right you can see the ensemble's predictions are equal to the sum of the predictions of the first two trees. Similarly, in the third row another tree is trained on the residual errors of the second tree.*


###### Properties:
- Gradient Boosting works well with [[regression]] tasks, like [[regression tree]]s
- [[scikit-learn]] has several [[boosting]] algorithms, such as Gradient Boosting 

###### Additional Thoughts:
