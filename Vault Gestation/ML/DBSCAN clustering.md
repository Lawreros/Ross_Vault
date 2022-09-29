name : DBSCAN clustering
tags : 
backlinks : 
source : https://www.analyticsvidhya.com/blog/2020/09/how-dbscan-clustering-works/

###### Content:
Density-Based Spatial Clustering of Applications with Noise (DBSCAN) is a density-based clustering algorithm that works on the assumption that clusters are dense regions in space separated by regions of lower density.

DBSCAN requires only two parameters: $\epsilon$ and *minPoints*. 
- $\epsilon$ being the radius of the circle to be created around each data point to check the density.
- *minPoints* being the minimum number of data points required inside of the circle for the data point to be classified as a **Core** point

The number of points within range of the circle for each data point is then used to classify points as being **Core** to a cluster, on the **Border** of a cluster, or **Noise** outside of any clustering. (*See source link for visuals/more explanation*)

###### Properties:
- The value of *minPoints* should be at least one greater than the number of dimensions of the dataset.
- The number clusters does not need to be defined ahead of time, like in [[k-means clustering]]
- The "best" value of $\epsilon$ can be decided using a [[k-distance graph]] and finding where the point of maximum curvature is

###### Additional Thoughts:
- The link in the source also has how to implement this clustering algorithm in sklearn/Python