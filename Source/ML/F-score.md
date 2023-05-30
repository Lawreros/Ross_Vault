name : F-score (F1-score)
tags : 
backlinks : 
source : https://deepai.org/machine-learning-glossary-and-terms/f-score, https://en.wikipedia.org/wiki/F-score

###### Content:
The F-score, also called the F1-score, is a measure of a model's accuracy on a dataset. It is used to evaluate [[binary classification]] models by combining the [[precision]] and [[recall]] of the model. The formula for the standard F1-score is: $$F_1 = 2*\frac{precision * recall}{precision + recall} = \frac{TP}{TP+0.5(FP+FN)}$$
Where $TP,FP$ and $FN$ are true positive, false positive, and false negative. The F1-score is the harmonic mean of both precision and recall, meaning it symmetrically represents both in one metric.

There is a generic version of the F-score, called the $F_\beta$ score, which applies additional weighting (in the form of $\beta$) in order to value either precision or recall more than the other.
$$F_\beta = (1+\beta^2) * \frac{precision * recall}{(\beta^2 * precision) + recall} = \frac{(1+\beta^2)TP}{(1+\beta^2)TP+\beta^2*FP+FN}$$
Where $\beta$ is a positive real factor chosen such that [[recall]] is considered $\beta$ times as important as precision is (see [[F2-score]]).

###### Properties:
- A perfect model has an F-score of 1, with the lowest score being 0
- Common adjusted F-scores are the [[F0.5-score]] and [[F2-score]]
- Similar to the [[Dice coefficient]], the F1-score is the Dice coefficient of the [[set]] of retrieved items and the set of relevant items.

###### Additional Thoughts:
