# Histopathologic-Cancer-Detection

## Introduction
This repository contains the solution to the Histopathologic Cancer Detection using Deep Learning. The goal of this project is to develop an algorithm to identify metastatic cancer in small image patches taken from larger digital pathology scans using deep learning techniques.

## Dataset Overview
The dataset consists of histopathologic scans of lymph nodes, where each image patch is labeled as either containing metastatic tissue or not. The train dataset contains 220,025 images, and the test set contains 57,468 images. The original dataset was derived from the Camelyon16 Challenge dataset, which contains 400 H&E stained whole slide images of sentinel lymph node sections.

## Data Pre-processing
- The train dataset is pre-processed to create a balanced subset of 160,000 samples, containing an equal number of positive and negative examples.
- Data augmentation techniques such as random horizontal and vertical flips, and random rotation are applied to the training data to enhance model performance.

## Technologies Used
- Python: Programming language used for data processing, model development, and evaluation.
- PyTorch: Deep learning framework used to build and train neural network models.
- OpenCV: Library used for image processing tasks.
- Matplotlib: Visualization library used to visualize images and data distributions.
- scikit-learn: Library used for various machine learning utilities and metrics computation.

## Model Architecture
- Convolutional Neural Network (CNN) architecture is utilized for image classification.
- The model architecture consists of multiple convolutional layers followed by max-pooling layers and fully connected layers.
- Activation functions such as ReLU and softmax are used to introduce non-linearity and produce class probabilities, respectively.

## Model Training and Evaluation
- The dataset is split into training and validation sets using a subset random sampler.
- The model is trained using the training set and evaluated on the validation set.
- Evaluation metrics such as ROC AUC score and accuracy are used to assess the performance of the model.
