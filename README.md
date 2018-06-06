# CS168
Classifier and Segmenter for Brachial Plexus Nerves

# Overview
This project consists of a classifer and a segmenter which can be used to achieve better results with respect to the ROI on tests where the nerve is present and not present.

# Works Used/Cite and Attributions
For this project, we based our implmentation on the following links:
https://towardsdatascience.com/medical-image-segmentation-part-1-unet-convolutional-networks-with-interactive-code-70f0f17f46c6
http://cv-tricks.com/tensorflow-tutorial/training-convolutional-neural-network-for-image-classification/

The implementation we based our classifier on is based off of the CNN classifier presented on the tensorflow tutorial website
https://www.tensorflow.org/tutorials/deep_cnn

The implementation we based our segmenter on is based off of the U-Net architecture that is presented in the following scholarly paper:
https://arxiv.org/pdf/1706.00712.pdf

The dataset we used can be found here:
https://www.kaggle.com/c/ultrasound-nerve-segmentation/data


# Dependancies
To run our project, one must have the both the data and the dependancies. Dependancies include:
pandas
numpy
matplotlib
tensorflow
dataset
opencv
sklearn
datetime
scipy

# Managing Data
For the classifier the data must be arragned as follows:
/train/NoNerve
/train/Nerve
where each folder only contains the respective ultrasound images (not the masks)

For the segmenter the data must be arranged as follows:
/masks/
/iamges/
where the former contains the masks and the latter contains the ultrasound images

# Utility
LabelingTool.ipynb is a tool that can be used to seperate the ultrasound images based on the presence of a nerve.
If the mean value of a mask (as a .tif) is 0.0, then there was no ROI and thus should be in the NoLegion category and vis versa.

