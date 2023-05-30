name : Hausdorff distance (HD)
tags : 
backlinks : 
source : https://arxiv.org/pdf/2006.14822.pdf, https://en.wikipedia.org/wiki/Hausdorff_distance#:~:text=The%20Hausdorff%20distance%20is%20the,point%20in%20the%20other%20set,
http://cgm.cs.mcgill.ca/~godfried/teaching/cg-projects/98/normand/main.html

###### Content:
Hausdorff distance is a metric used by [[segmentation model]]s in order to track performance, but can be used for comparing the distance between any two [[set]]s. It is defined as $$hd(X,Y) = max_{x\in X}min_{y\in Y} ||x-y||_2$$
Where $hd(X,Y)$ is the Hausdorff distance between sets $X$ and $Y$, and $||\cdot||_2$ is the [[L2 norm]]. Thus, the Hausdorff distance is the largest minimum distance between the two sets.

![[Hausdorff_distance.png]]
The above image shows an example of two sets $X$ and $Y$ with two potential Hausdorff distances $d_{XY}$ and $d_{YX}$, where $d$ stands for distance ($||\cdot ||_2$ or some other distance metric).


A good way to think about it is:
 *"The Hausdorff distance is the longest distance you can be forced to travel by an adversary who chooses a point in one of the two sets, from where you then must travel to the other set. In other words, it is the greatest of all the distances from a point in one set to the closest point in the other set."*

###### Properties:
- There seems to be some inconsistency in terminology. Depending on the source, "Hausdorff distance" may be the collection of Hausdorff distances for each point in a set $X$ to the points of set $Y$, with "maximum Hausdorff distance" being the largest of all measurements.
- **95% HD** or **Hausdorff distance (95%)**: 
  Very similar to the Hausdorff distance, except is is the 95th percentile of the distances between boundary points in X and Y. The purpose for using this metric is to eliminate the impact of a very small subset of the outliers.

###### Additional Thoughts:

