# Image-Recognition

This project will focus on an image recognition problem. 
I will construct a variety of machine learning models with the goal of generating predictive classifications.

The Data

The MNIST Fashion database (https://github.com/zalandoresearch/fashion-mnist) 
collected a large number of images for different types of apparel. 
Each image is divided into small squares called pixels of equal area. 
Within each pixel, a grayscale brightness measurement was recorded. 
The brightness values range from 0 (white) to 255 (black). The original data set divided each image into 784 (28 by 28) pixels.
To facilitate easier computation, we have condensed these data into 49 pixels (7 by 7) per image. 
The first 7 pixels represent the top row, the next 7 pixels form the second row, etc.

The following files are also provided here:

Training Set: MNIST-fashion training set-49.csv. This file contains 60,000 rows of data.
Testing Set: MNIST-fashion testing set-49.csv. This file contains 10,000 rows of data.

Each file includes the following columns:

label: This provides the type of fashionable product shown in the image.
pixel1, pixel2, …, pixel49: These columns provide the grayscale measurement for the 49 pixels of the image.

The Challenge

What are the best machine learning models for classifying the labels of the testing set based upon the data of the training set? 
How small of a sample size do we need to generate the “best” predictions? 
To balance these competing goals, I will introduce an overall scoring function:

Points = 0.5 * A + (1 - B)

where

A is the proportion of the training rows that is utilized in the model. For instance, if we use 30,000 of the 60,000 rows, then A = 30,000 / 60,000 = 0.5; and

B is the testing accuracy. This is the proportion of the predictions on the testing set that are correctly classified. For instance, if 9,000 of the 10,000 rows are correctly classified, then B = 9,000 / 10,000 = 0.9.
