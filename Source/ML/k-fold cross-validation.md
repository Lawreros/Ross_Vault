name : k-fold cross-validation
tags : 
backlinks : 
source : 

###### Content:
In k-fold [[cross-validation]], the original sample is randomly partitioned into k equal sized subsamples. Of the k subsamples, a single subsample is retained as the validation data for testing the model, and the remaining k − 1 subsamples are used as training data. The cross-validation process is then repeated k times, with each of the k subsamples used exactly once as the validation data. The k results can then be averaged to produce a single estimation.

###### Properties:
- The advantage of this method over repeated random sub-sampling (see below) is that all observations are used for both training and validation, and each observation is used for validation exactly once.
- 10-fold cross-validation is a very commonly used version of this method

###### Additional Thoughts:
