# Neural-Net-Demosaic AKA Coloury

# Problem
Nearly all digital cameras capture a mosaic and must run this into a demosaicing algorithm to predict the raw image. This program uses a CNN trained on hundreds of images gathered
from the internet to accurately predict the raw image.
# Data
Gathered images are proccessed down to a standard size and mosaiced to emulate raw photo data, the colour values of each pixel are then taken as the features and the targets. 
The program uses a 9x9 of the target pixel's neighbors as features. The data is broken into training validation and test sets.
# Model
The CNN model consists of 5 layers including the input and output layers with 2 of them as Convolutional. The final hidden layer uses l2 regularization to reduce overfitting, whose
values are chosen using the validation set. The training is also done in 2 epochs with batches of 64 to increase training speed. The optimizer is adam.
# Metrics
The network uses mean squared error as a loss function to punish large discrepencies harsher. 

# Overall
This model vastly out performed the build in matlab demosaic function by up to 10x. The final test showed a mean squared error of 8.7944 with an accuracy of 0.9452
