name : precision
tags : 
backlinks : 
source : #HOML 

###### Content:
A metric for measuring the performance of a classifier. The precision of a model is the number of true positives (correct classifications) divided by the total number of positives (true positives and false positives):
$$ precision = \frac{TP}{TP+FP}$$
With perfect precision returning a value of 1.

###### Properties:
- This metric is flawed, as a model only classifying one data point as positive while ignoring all other positives would still result in perfect precision. To account for this, precision is often used along another metric called [[recall]].
- Increasing precision reduces [[recall]] and vice versa

###### Additional Thoughts:
