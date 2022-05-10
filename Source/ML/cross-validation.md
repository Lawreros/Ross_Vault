name : cross-validation (out-of-sample testing)
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/Cross-validation_(statistics)

###### Content:
Cross-validation is a resampling method that uses different portions of the data to test and train a model on different iterations. It mainly is used in settings where the goal is prediction, and the user wants to measure how a predictive model will perform in practice. This is done by taking a dataset whose's labels are known and partitioning the data into a training set and testing set. The model is trained on the training set and then has it's performance tested using the testing set.

How the training and testing sets are partitioned can follow several different methods. Some common methods of cross-validation are:
[[leave-one-out cross-validation]]
[[k-fold cross-validation]]
[[Monte Carlo cross-validation]]

###### Properties:
- Mainly used with classifiers
- The quantitative measure of fit that is used to determine the performance of the model can vary based on what is appropriate for the data and model. For [[binary classification]] problems the measure could be the rate at which the model correctly predicted the [[classification]] of a data point. When the value being predicted is continuously distributed, the [[mean squared error]], [[root mean squared error]], or [[median absolute deviation]] could be used to summarize the errors

###### Additional Thoughts:
