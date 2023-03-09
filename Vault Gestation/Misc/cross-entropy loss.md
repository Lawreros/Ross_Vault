name : cross-entropy loss
tags : 
backlinks : 
source : https://machinelearningmastery.com/cross-entropy-for-machine-learning/, https://ml-cheatsheet.readthedocs.io/en/latest/loss_functions.html, https://towardsdatascience.com/cross-entropy-loss-function-f38c4ec8643e

###### Content:
Cross-[[entropy]] loss, measures the performance of a [[classification model]] whose output is a probability value between 0 and 1. For example, if the desired output of a model is `[1,0,0,0]` for a input with class `1` and the model outputs `[0.775, 0.116, 0.039, 0.070]`, cross-entropy can be used for a [[loss function]] to get the probability outputs as close to the true values.

In [[binary classification]], where the number of classes $M$ equals 2, cross entropy can be calculated for each model output as: $$-(ylog(p)+(1-y)log(1-p))$$ 
If $M > 2$ (i.e. multiclass classification), we calculate a separate loss for each class label per observation and sum the result: $$-\sum_{c=1}^M y_{o,c}log(p_{o,c})$$
Where $M$ is the number of classes, $log$ is the natural log, $y$ is the binary indicator (0 or 1) if class label $c$ is the correct classification for observation $o$, and $p$ is the predicted probability observation $o$ is of class $c$.

###### Properties:
- Cross-entropy loss increases as the predicted probability diverges from the actual label. So predicting a probability of .012 when the actual observation label is 1 would be bad and result in a high loss value. A perfect model would have a log loss of 0.

![[Pasted image 20221215180616.png]]
- The graph above shows the range of possible loss values given a true observation (isDog = 1). As the predicted probability approaches 1, log loss slowly decreases. As the predicted probability decreases, however, the log loss increases rapidly. Log loss penalizes both types of errors, but especially those predictions that are confident and wrong!
- Cross-entropy is not [[log loss]], but they calculate the same quantity when used as [[loss function]]s for [[classification]] problems
- Cross-entropy struggles when there is a [[class imbalance]], as it aims to penalize the wrong predictions more than reward the correct predictions, see [[focal loss]] or [[balanced cross-entropy loss]] for an alternative.

###### Additional Thoughts:
