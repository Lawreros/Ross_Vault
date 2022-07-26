name : bagging (bootstrap aggregation, bootstrapping)
tags : 
backlinks : 
source : https://www.ibm.com/cloud/learn/bagging, #HOML 

###### Content:
Bagging, also known as bootstrap aggregation, is the [[ensemble learning]] method that is common used to reduce variance within a noisy dataset. In bagging, a random sample of data in a training set is selected *with replacement* and used to train a model. After several samples are generated, the average or majority of the predictions from these weak models yield a *more accurate* estimate.

*Note: Bagging is different from [[boosting]], as bagging can be done in parallel instead of boosting which is done is sequence.*

###### Properties:
- Bagging can reduce the [[variance]] within a learning algorithm. This is particularly helpful with [[high-dimensional]] data, where missing values can lead to higher variance, making it more prone to [[overfit]]ting and preventing accurate generalization to new datasets.
- It is difficult to draw very precise insights through bagging due to the averaging involved across predictions.
- Bagging slows down and grows more computationally intensive as the number of iterations increases.
- Bagging works well with algorithms that are less stable. One that are more stable or subject to high amounts of [[bias]] do not provide as much benefit as there's less variation within the dataset of the model. *"Bagging a [[linear regression]] model will effectively just return the original predicitons for larg enough $b$"*

###### Additional Thoughts:
