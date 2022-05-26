## Kaggle project

### Links:
- Exploring the data: https://www.kaggle.com/code/eduardofarina/welcome-to-the-competition-eda
- Pytorch beginner tutorial: https://pytorch.org/tutorials/beginner/basics/quickstart_tutorial.html
- Pytorch training a classifier: https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html
- Multi-Label Image Classification with PyTorch: https://learnopencv.com/multi-label-image-classification-with-pytorch-image-tagging/


### Working notes:
- There are both MONOCHROME1 and MONOCHROME2 images in the dataset. I need to investigate further as to what this means for training.
		- Doesn't look like it changes any values, just whether max = white or max=black
- It's clear that I don't really understand Pytorch as well as I should, I really need to revisit the capabilities of it. Maybe incorporate the notes from it into obsidian? No, first I learn enough to train my model. While it runs, that's when I add information to obsidian. I *need* to get things that actually run for me to keep any sort of momentum

Notes from "Multi-Label Image..." link
- By the looks of things, I want to make a **multi-label** classifier, as opposed to **multi-class** classifier. The difference being that multi-class assumes that each image only has one and only one label out of the set of target labels. Mulit-label assumes multiple labels for a given image (i.e. for a  picture of a smiling person it would give labels `smiling`, `eyes`, `brown hair`)
- 


### Coding notes:
- `pydicom` is the standard for loading dicom data
		- `pydicom.dcmread(file, stop_before_pixels=True)` only loads the metadata for each dicom file

- `map` function in python: geeksforgeeks.org/python-map-function/


### Things to Investigate:
- It's probably best to use already existing networks for starting my models. This is a good starter link for ResNets: https://towardsdatascience.com/understanding-and-visualizing-resnets-442284831be8
		- I need to make a list of common models, that way I can possibly reference them when talking in interviews.