# Deep Learning for Sign Language Recognition
Zimu Su

## Abstract
Deaf people mostly use sign language to communicate. While most people do not understand sign language if they are not trained, it is necessary to develop a translator from sign language to English for better communication of deaf people. This project aims to use deep learning modeling to recognize the hand gestures corresponding to certain sign language word. Datasets from [Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) is employed for the project. Custom 3-layer CNN model, MobileNetV2 used EfficientNetB0 have been employed for data training and the accuracy scores reaches >98% for the image sets provided by the dataset.

## Design
There are 29 classes of images which respectively correspond to 26 letters, and specific meaning of delete, space and nothing. One image includes a hand gesture (or no hand gesture) corresponding to a specific sign. There are 87,000 images in the training set and 3,000 images for each classes.

## Data
Training data are collected from [Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet). Test data are respectively provided by the dataset and photos taken by myself.

## Algorithms
OpenCV is employed for converting images to arrays. Keras also includes image-to-array function but its algorithm is different from OpenCV, and its score is not good (training score: 0.8769, validation score: 0.2641).

Custom CNN model is built for training the dataset using Google colab platform. The CNN model contains 3 layers, each of which contains convolution layer, batch normalization (for image information generalization), drop out (for preventing overfitting). Images of single channel are trained in the model.

The datasets are also trained through transferring modeling of MobileNetV2 and EfficientNetB0.

## Tools
Numpy, Pandas, Keras, OpenCV

## Communication
The project is under supervision of Kevin Chiv and delivered on 10/05/2022.
