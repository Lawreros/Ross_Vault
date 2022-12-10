name : image classification
tags : 
backlinks : 
source : https://huggingface.co/tasks/image-classification

###### Content:
Image Classification is a fundamental [[supervised learning]] task that attempts to comprehend an entire image as a whole. The goal is to classify the image by assigning it to a specific label. Typically, Image Classification refers to images in which only one object appears and is analyzed. 

In contrast, [[object detection]] involves both classification and localization tasks, and is used to analyze more realistic cases in which multiple objects may exist in an image.

###### Properties:
- Early computer vision models relied on raw pixel data as the input to the model. However, raw pixel data alone doesn't provide a sufficiently stable representation to encompass the myriad variations of an object as captured in an image. The position of the object, background behind the object, ambient lighting, camera angle, and camera focus all can produce fluctuation in raw pixel data; these differences are significant enough that they cannot be corrected for by taking weighted averages of pixel RGB values.

###### Additional Thoughts:
