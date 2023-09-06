# Project Ideas:
This note is where I'll store ideas about future personal projects while expanding my skillset
## Segmentation Practice:
#### 3D $U^2$-Net; A 3D Universal U-Net for Multi-Domain Medical Image Segmentation
- https://paperswithcode.com/paper/3d-u2-net-a-3d-universal-u-net-for-multi
##### Why do this project?
- Good refresher on U-Net as well as 3D segmentation
- Covers combining different medical modalities
- Low resource requirements
- Good practice for UNETR

##### Dataset:
- Medical Segmentation Decathlon challenge: https://decathlon.grand-challenge.org/
	- Collection of MRI and CT data for different 
	- Free to download

#### UNETR: Transformers for 3D Medical Image Segmentation
- https://paperswithcode.com/paper/unetr-transformers-for-3d-medical-image
##### Why do this project?
- Teaches about segmentation thought the use of a whole bunch of different ML layer types and architectures
	- Deconvolutional layers https://towardsdatascience.com/types-of-convolutions-in-deep-learning-717013397f4d
	- embedding layers and linear projections
	- normalization
	- etc
- Is legitimately impressive

##### Dataset:
- Beyond the Cranial Vault (BTCV) https://www.synapse.org/#!Synapse:syn3193805/wiki/217753
	- Collection of abdominal CT images with different organs segmented
Medical Segmentation Decathlon challenge: https://decathlon.grand-challenge.org/
	- Collection of MRI and CT data for different 
	- Free to download


#### 3D MRI brain tumor segmentation using autoencoder regularization:
- https://paperswithcode.com/paper/3d-mri-brain-tumor-segmentation-using
##### Why do this project?
- Teaches about automated segmentation
- Teaches about autoencoder
- Is a method which is geared for making the most out of a limited dataset
##### Dataset: 
- BraTS dataset 2020: https://www.med.upenn.edu/cbica/brats2020/data.html
	- In the paper they use a different year's dataset, but that shouldn't really matter for this practice
	- Could also use the `Liver Tumor Segmentation` dataset instead


#### Attention Enriched Deep Learning Model for Brest Tumor Segmentation in Ultrasound Images:
- https://paperswithcode.com/paper/attention-enriched-deep-learning-model-for
##### Why do this project?
- Teaches about segmentation
- Shows that I know how to work with ultrasound
- Learn about visual saliency (layer of image for directing radiologist's attention)
- Learn about Dice similarity coefficient

##### Dataset:
- Paper referencing dataset BUSIS: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9025635/
- Link for application of dataset: http://cvprip.cs.usu.edu/busbench/
	- Need to apply for access and wait possibly 10 days to hear back from them
	- They also have requirements for using their data, mainly involving citing all of their stuff
	- Found a version of it that is easy for download and doesn't require the approval process. Unfortunately the dataset seems to be pngs, which kind of sucks but might be acceptable for the first tests.  https://academictorrents.com/details/d0b7b7ae40610bbeaea385aeb51658f527c86a16

### Interesting Datasets:

There's a giant list of datasets here: https://www.datasetlist.com/

##### Liver Tumor Segmentation:
- 130 CT scans for segmentation of the liver as well as tumor lesions (saved across both parts)
- Saved as nifiti files, with the segmentation files having an intensity value of 1 for the liver and 2 for tumor
- LINK (part 1): https://www.kaggle.com/datasets/andrewmvd/liver-tumor-segmentation/versions/5?resource=download
- LINK (part 2): https://www.kaggle.com/datasets/andrewmvd/liver-tumor-segmentation-part-2


##### Autism Brain Imaging Data Exchange (ABIDEII):
- Big collection of MRI data for control and autistic individuals
- LINK: http://fcon_1000.projects.nitrc.org/indi/abide/abide_II.html

##### Pancreas:
- Paper: https://link.springer.com/chapter/10.1007/978-3-319-24553-9_68
- Download: https://wiki.cancerimagingarchive.net/display/Public/Pancreas-CT#225140407e328bff74a84d4885648246b4de92a4
- 82 abdominal 3D CT scans with and without cancer lesions/major abdominal pathologies

---

### Classification Practice:
#### Source Paper:

##### Why do this project?

##### Dataset


#### Source Paper:

##### Why do this project?

##### Dataset


---
### Large Database Analysis Practice:
#### Source Paper:

##### Why do this project?

##### Dataset


#### Source Paper:

##### Why do this project?

##### Dataset
