name : class imbalance
tags : 
backlinks : [[balanced cross-entropy loss]], [[focal loss]]
source : https://machinelearningmastery.com/what-is-imbalanced-classification/

###### Content:
Class imbalance simply refers to when there is a significant imbalance in the number of examples for the different classes in a training set for a [[classification model]]. This results in biases with the calculation of the [[loss function]]s used for training such predictive models.

Say that your training set contains 200 examples of category A for every example of category B. The majority class examples will dominate the loss function and gradient descent, causing the weights to update in the direction of the model becoming more confident in predicting the majority class while putting less emphasis on the minority classes.

###### Properties:
- [[object detection]] is a great example of this, as the number of pixels related to the object you are trying to detect are often significantly less than the rest of the image (i.e. the background).

###### Additional Thoughts:
