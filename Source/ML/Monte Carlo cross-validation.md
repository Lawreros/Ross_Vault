name : Monte Carlo cross-validation (Repeated random sub-sampling validation)
tags : 
backlinks : 
source : 

###### Content:
A [[cross-validation]] method which creates multiple random splits of the dataset into training and testing data. For each split, the model is trained on the training data, and predictive accuracy is assessed using the model's performance on the testing data.

###### Properties:
- The advantage of this method (over [[k-fold cross-validation]]) is that the proportion of the training/testing split is not dependent on the number of iterations (i.e., the number of partitions). 
- The disadvantage of this method is that some observations may never be selected in the validation subsample, whereas others may be selected more than once. In other words, validation subsets may overlap. This method also exhibits Monte Carlo variation, meaning that the results will vary if the analysis is repeated with different random splits.
- As the number of random splits approaches infinity, the result of repeated random sub-sampling validation tends towards that of leave-p-out cross-validation.

###### Additional Thoughts:
