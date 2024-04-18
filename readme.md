# Breast classification README

## Description

This project is neural network in Python to classify breast cancer into two groups: benign and malignant from
histopathological
images.

## Dataset

Dataset used in this project is The Breast Cancer Histopathological Image Classification (BreakHis).
It is composed of 9,109 microscopic images of breast tumor tissue collected from 82 patients using different magnifying
factors (40X, 100X, 200X, and 400X). To date, it
contains 2,480 benign and 5,429 malignant samples (700X460 pixels, 3-channel RGB, 8-bit depth in each channel, PNG
format).

## Goal

The goal of this project is to create a neural network that will classify breast cancer into two groups: benign and
malignant, while achieving the highest possible accuracy.

## Preprocessing

The images were preprocessed by resizing them to 128x128 pixels and normalizing them. Also due to fact that the dataset
is imbalanced, the images were augmented by rotating, flipping, zooming, and shifting them. The augmented images were
then split into training and validation sets. The training set was further split into training and validation sets.

## Model

The model used in this project is a convolutional neural network (CNN):
VGG-16 architecture with additional layers added to it, to achieve better results.
Those layers contain functions like flatten, dense, normalization and dropout.
Dense function was designed to learn features based on the output from the previous layer. Activation of "relu"(unit
linear threshold function) is used to introduce nonlinearity in the model.
The Dropout layer randomly shuts down some of the neurons during training, helping to regularize the model and prevent
overtraining.

## Results

The model achieved high accuracy: 86.32%. To analyze the results further, plots such as the ROC curve, Precision-Recall
curve, and Confusion Matrix were created. To fully understand the model's learning process, a Grad-CAM heatmap was
developed. The purpose was to be able to see which image fragments were considered classification-worthy by the network.

## Technologies

- Python
- Keras
- Matplotlib
- Numpy
- Tensorflow
