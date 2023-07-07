name : Intersection over Union (IoU, Jaccard Index)
tags : 
backlinks : 
source : https://medium.com/analytics-vidhya/iou-intersection-over-union-705a39e7acef , https://machinelearningspace.com/intersection-over-union-iou-a-comprehensive-guide/

###### Content:
The IoU is a measure used to evaluate the extent of overlap between two boxes (similar to the [[Dice coefficient]]). IoU is mainly used in applications related to [[object detection]], where a model is trained to output a box that fits perfectly around an object. It is computed as the ratio of intersection of the predicted bounding box and the ground truth bounding box to the union of the two bounding boxes.

$$IoU  = \frac{|X\cap Y|}{|X\cup Y|} =  \frac{|X\cap Y|}{|X|+|Y|-|X\cap Y|} = \frac{TP}{TP+FP+FN}$$
where $X$ and $Y$ are two bounding boxes, and $TP,FP,FN$  are true positive, false positive, and false negative.


###### Properties:
- IoU values can range from $[0,1]$, with 1 being perfect agreement
- For [[binary classification]] or [[multi-class segmentation]], the mean IoU of the image is calculated by taking the IoU of each class and averaging them. 

###### Additional Thoughts:
- For implementation of IoU in numpy and PyTorch, see here: https://hasty.ai/docs/mp-wiki/metrics/iou-intersection-over-union