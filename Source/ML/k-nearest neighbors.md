name : k-nearest neighbors (k-NN)
tags : 
backlinks : 
source : 

###### Content:
The k-NN algorithm is a [[supervised learning]] algorithm which is used for [[classification]], where the output is a class membership for the input object (feature vector). An object is classified by a plurality vote of its neighbors, with the class most common between the $k$ "nearest" neighbors.
The "training" phase of the algorithm consists only of storing the feature vectors and class labels of the training samples (i.e. use vectors that you already know the [[classification]] of). In the classification phase, $k$ is a user-defined constant, and each input feature vector is classified based upon the classification of the $k$ nearest neighbors from the training samples.


###### Properties:
- Since this algorithm relies on distance for classification, if the features represent different physical units or come in vastly different scales then normalizing the training data can improve accuracy dramatically.
- A commonly used distance metric for continuous variables is [[Euclidean distance]]
- see [[k-nearest neighbors graph]] and [[k-distance graph]]

###### Additional Thoughts:
