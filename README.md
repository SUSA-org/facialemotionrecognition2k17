# Facial Emotion Recognition - SUSA Data Consulting Fall 2017

This repository contains the work completed by SUSA for [IPMD Inc](http://www.ipmdinc.com/) during the Fall 2017 Semester. The project was to classify facial emotions of a dataset of images provided by a Kaggle competition released in 2013. The data provided is fraught with mislabelling and inconsistent cropping of faces. Our final validation accuracy acheived on this dataset was 65% using an ensemble model of max-pooling convolutional neural networks, along with ResNet-like architectures. 


## Code

The code provided is how we trained our ensemble models with a 4-fold cross validation on 28,000 training images (48x48x3).

***splitscript.sh***

This is a bash script to be run to train our models on all 4 cross-validation folds of the provided data. 

***model_train.py***

Script to train either a Max-pooling CNN or ResNet-like architecture depending on flags passed. Saves models to exp\_{fold\_num}/.

## Data

This data is not provided due to size limits. The following information for internal docs on understanding the code.

***train.npz***

Training data provided as "PublicUse" in the (Kaggle Competition data)[https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data]

***test.npz***

Data used to evaluate the model after validation & hyper parameter tuning. Provided as "PrivateUse" (used for the leaderboard rankings).
