name : ROC curve (reciever operating characteristic curve)
tags : 
backlinks : 
source : #HOML 

###### Content:
A common tool used with [[binary classification]] problems. It is very similar to the [[precision]]/[[recall]] curve, but instead of plotting precision versus recall, the ROC curve plots the true positive rate (aka [[recall]]) against the [[false positive rate]]. The ROC curve plots [[recall]] versus 1-[[specificity]].

![[Pasted image 20220313190658.png]]

Note that there is a tradeoff: the higher the recall, the more false positives that classifier poduces. The dotted line represents the ROC curve of a purely random classifier. A good classifier stays as far away from that line as possible.
One way to compare classifiers is to measure the [[AUC]] (area under the curve).

###### Properties:


###### Additional Thoughts:
