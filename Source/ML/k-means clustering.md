name : k-means clustering
tags : 
backlinks : 
source : https://en.wikipedia.org/wiki/K-means_clustering

###### Content:
k-means clustering is a method of vector quantization that aims to partition $n$ observations into $k$ clusters in which each observation belongs to the cluster with the nearest mean (cluster centroid).

Given a set of observations $(x_1, x_2,..., x_n)$ where each observation is a $d$-dimensional real vector, $k$-means clustering aims to partition $n$ observations into $k < n$ sets $S = \{S_1,S_2,...,S_k\}$ so as to minimize the within-cluster sum of squares.

**Iterative Process:**
Given an initial set of $k$ means $m_1^{(1)},...,m_k^{(1)}$, the algorithm proceeds by alternating between two steps:
*Assignment step:* Assign each observation to the cluster with the nearest mean, using the least squared [[Euclidean distance]] : $$S_i^{(t)} = \{x_p:||x_p-m_i^{(t)}||^2 \leq ||x_p-m_j^{(t)}||^2 \forall j, 1 \leq j \leq k\}$$ where each $x_p$ is assigned to exactly one $S^{(t)}$.
*Update step:* Recalculate the means for observations assigned to each cluster: $$m_i^{(t+1)}= \frac{1}{|S_i^{(t)}|}\sum_{x_j \in S_i^{(t)}x_j$$ In other words, for each [[classification]] $S_i$ you sum all vectors associated with the class and divide by the number of vectors which were classified as $S_i$

###### Properties:
- This algorithm is not guaranteed to find the optimum and fails at creating clusters of more complicated shapes (think concentric circles where each circle is a different category)
- Commonly used initialization methods for the means $m_i$ are to either randomly choose $k$ observations from the dataset and use these as initial means (Forgy method), or randomly assign each observation to a classification and take the means from those (Random Partition method).
- $NP$-hard for general Euclidean space (of d dimensions) even for two clusters

###### Additional Thoughts:
