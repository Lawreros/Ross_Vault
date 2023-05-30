name : Dice coefficient (Sorensen-Dice index)
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/S%C3%B8rensen%E2%80%93Dice_coefficient, https://www.jeremyjordan.me/semantic-segmentation/

###### Content:
The dice coefficient is used to measure the similarity between two sets of data. This index has become arguably the most broadly used tool in the validation of [[segmentation model]]s, but it is a much more general concept which can be applied to sets of data for a variety of applications including [[natural language processing]]. The equation for this metric is:
$$DC = \frac{2|X\cap Y|}{|X| + |Y|}$$ where $|X|$ and $|Y|$ are the [[cardinality]] of each set for a given value. In other words, if you are calculating the Dice coefficient for two images with pixel values of either 0 or 1, then $|X|$ would be the number of pixels with intensity 1 in the image $X$.

For the case of evaluating a Dice coefficient on predicted segmentation masks, where $X$ is the prediction and $Y$ is the ground truth, we can **approximate** $|X\cap Y|$ as an element-wise multiplication between the prediction and target mask, and then sum the resulting matrix:
$$|X\cap Y| = \begin{bmatrix} 0.01 & 0.02 & 0.01 \\
0.05 & 0.12 & 0.04 \\
0.94 & 0.92 & 0.98 \\
0.99 & 0.98 & 0.99 \\
\end{bmatrix}*\begin{bmatrix} 0 & 0 & 0 \\
0 & 0 & 0 \\
1 & 1 & 1 \\
1 & 1 & 1 \\
\end{bmatrix} \rightarrow \begin{bmatrix} 0 & 0 & 0 \\
0 & 0 & 0 \\
0.94 & 0.92 & 0.98 \\
0.99 & 0.98 & 0.99 \\
\end{bmatrix} \rightarrow 5.8$$
and $|X|$ is either the element-wise sum of probabilities, or the squared sum of probabilities (up to you), and the same with $|Y|$.

When applied to Boolean data, using the definition of true positive (TP), false positive (FP), and false negative (FN), it can be written as: $$DC = \frac{2TP}{2TP+FP+FN}$$

###### Properties:
- While Dice coefficients are calculated for binary segmentations, for multiple classes there exists the [[generalized Dice coefficient]]

###### Additional Thoughts:
