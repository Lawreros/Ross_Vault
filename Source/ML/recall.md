name : recall (sensitivity, true positive rate)
tags : 
backlinks : 
source : #HOML 

###### Content:
A metric for measuring the performance of a classifier. Recall is the ratio of positive instances that are correctly detected by the classifier to all instances labeled as positive by the classifier. 

$$recall = \frac{TP}{TP+FN}$$

###### Properties:
- This metric is flawed, as a model classifying all data points as positive while would result in perfect recall. To account for this, precision is often used along another metric called [[precision]].
- Increasing recall reduces [[precision]] and vice versa

###### Additional Thoughts:
