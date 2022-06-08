## Kaggle project
[X] Organize training data in a meaningful way
		[X] Create data loader
		[X] Account from Monochrome2
[X] Organize testing data
[X] Create model
		[] Simple 2 layer CNN
		[] Create accuracy/performance metric (Mean F1 score: https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier/overview/evaluation)
[] Refine model	
	

### Links:
- Exploring the data: https://www.kaggle.com/code/eduardofarina/welcome-to-the-competition-eda
- Pytorch beginner tutorial: https://pytorch.org/tutorials/beginner/basics/quickstart_tutorial.html
- Pytorch training a classifier: https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html
- Multi-Label Image Classification with PyTorch: https://learnopencv.com/multi-label-image-classification-with-pytorch-image-tagging/


### Working notes:
- There are both MONOCHROME1 and MONOCHROME2 images in the dataset. I need to investigate further as to what this means for training.
		- Doesn't look like it changes the distribution values, just whether max = white or max=black
		- Actually, according to https://daily-blog.netlify.app/questions/2402091/index.html , I might be able to standardize the input values independent of what Monochrome they are, or how they have been collected:
				- It looks like "real intensity" = "Rescale Slope" X "stored value" + Rescale Intercept (https://www.kitware.com/dicom-rescale-intercept-rescale-slope-and-itk/)
		- Nope, I was right the first time, I just need to add a check which converts Monochrome2 into Monochrome1 before submitting to training.
- Huh, in the data exploration Kaggle notebook, they randomly invert the images they are given. I guess that lends credence to making a model that ignores Monochrome1/2 distinctions.
- They also for some reason do `img = img/img.max - 0.5` which would make it a `[-0.5, 0.5]` range for a 

- It's clear that I don't really understand Pytorch as well as I should, I really need to revisit the capabilities of it. Maybe incorporate the notes from it into obsidian? No, first I learn enough to train my model. While it runs, that's when I add information to obsidian. I *need* to get things that actually run for me to keep any sort of momentum

- There really isn't some "tried and true" way to make data the same size for training. That's kind of a bummer, since I am pretty skeptical as to the model getting too much information based on which areas are blacked out.
		- Going to have to look into transformations to the input to improve the validity

- So I'm just going to convert the images to png's and normalize them according to what pytorch's version of ResNext wants (https://pytorch.org/hub/pytorch_vision_resnext/)

```python
from torchvision import transforms
input_image = Image.open(filename)
preprocess = transforms.Compose([
    transforms.Resize(256),
    transforms.CenterCrop(224),
    transforms.ToTensor(),
    transforms.Normalize(mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225]),
])
```




Notes from "Multi-Label Image..." link
- By the looks of things, I want to make a **multi-label** classifier, as opposed to **multi-class** classifier. The difference being that multi-class assumes that each image only has one and only one label out of the set of target labels. Mulit-label assumes multiple labels for a given image (i.e. for a  picture of a smiling person it would give labels `smiling`, `eyes`, `brown hair`)

- Damn, ResNext is taking too damn long (that or loading the dicom data is taking too long). I need to find a faster and simpler model to use to train properly
- List of other pretrained image networks are found here: https://pytorch.org/vision/stable/models.html
- It seems like people are loading in this dataset: https://www.kaggle.com/datasets/ibombonato/xray-body-images-in-png-unifesp-competion
		-	This guy seemed to be using the png images and got a good enough score to be top 10: https://www.kaggle.com/code/alexanderyyy/xraybodyparts-fastai/notebook?scriptVersionId=97031156 

- Need to get the F-1 code working


### Coding notes:
- `pydicom` is the standard for loading dicom data
		- `pydicom.dcmread(file, stop_before_pixels=True)` only loads the metadata for each dicom file

- `map` function in python: geeksforgeeks.org/python-map-function/


### Things to Investigate:
- It's probably best to use already existing networks for starting my models. This is a good starter link for ResNets: https://towardsdatascience.com/understanding-and-visualizing-resnets-442284831be8
		- I need to make a list of common models, that way I can possibly reference them when talking in interviews.
		- ResNets for some reason need the model weights to be `double` datatype. This means you need: `model = Model_v1.double()`

- Top-N accuracy
- 