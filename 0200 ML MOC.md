# 0200 ML MOC
Machine Learning is the science (and art) of programming computers so they can learn from data.

Associated Tags: 

#### Common Concepts
- [[batch learning]]
- [[online learning]]
- [[instance-based learning]]
- [[model-based learning]]
- [[linear classifier]]
- [[ensemble learning]]


#### Supervised Learning ([[supervised learning]])
In supervised learning, the training data you feed the algorithm includes the desired solutions, called *labels*:
- [[k-nearest neighbors]]
- [[linear regression]]
- logistic regression
- [[support vector machine]] (SVMs)
		- Linear SVM Classification [[linear SVM]]
			- Hard Margin Classification
			- Soft Margin Classification
		- Nonlinear SVM Classification [[nonlinear SVM]]
			- Polynomial Kernel
			- Adding Similarity Features
			- Gaussian RBF Kernel
			- Computational Complexity
		- SVM Regression
- [[decision tree]]
- [[random forest]]
- neural networks

#### Unsupervised Learning ([[unsupervised learning]])
In unsupervised learning, the training data is unlabeled, causing the system to try a learn without a teacher.
- Clustering:
		- [[k-means clustering]]
		- [[DBSCAN clustering]]
		- hierarchical clustering analysis (HCA)
- Anomaly detection and novelty detection
		- one-class SVM
		- isolation forest
- Visualization and dimensionality reduction
		- principal component analysis (PCA)
		- kernel PCA
		- locally-linear embedding (LLE)
		- t-distributed stochastic neighbor embedding (t-SNE)
- Association rule learning
		- Apriori
		- Eclat

#### Semisupervised learning ([[semisupervised learning]])
Algorithms that can deal with partially labeled training data, usually a lot of unlabeled data and a little bit of labeled data.
-	deep belief networks (DBNs)
-	restricted Boltzmann machines (RBMs)

#### Performance Metrics
- [[cross-validation]]
- [[confusion matrix]]
- [[precision]]
- [[recall]]
- [[ROC curve]]
- [[AUC]]
- cross entropy loss

### Common Datasets:
- CIFAR
- MNIST

### Common Models:
- ResNet
		- https://towardsdatascience.com/introduction-to-resnets-c0a830a288a4
		- https://towardsdatascience.com/understanding-and-visualizing-resnets-442284831be8
- VGG
- UNet: https://analyticsindiamag.com/my-experiment-with-unet-building-an-image-segmentation-model/
		- Good example: https://www.kaggle.com/code/mateuszbuda/brain-segmentation-pytorch

## Topics to Investigate
- Linear Discriminant Analysis
- Marqardt Backpropagation Algorithm
- Canonical Correlation Analysis
- Stepwise Discriminant Analysis