# ASPP_Project
Project for Graduate Course in Advanced Scientific Programming in Python - Uppsala University
---------------------------------------------------------------------------------------

MNIST_Classification.ipynb is a Jupyter notebook to run a simple convolutional neural network classification on the MNIST dataset (http://yann.lecun.com/exdb/mnist/). The dataset consists of 60,000 samples for training and a test set of 10,000 samples of handwritten digits. The digits have been size-normalized and centered in a fixed-size image. The input images have the dimensions [28,28,1]

It uses torch as a backend for this machine learning task and uses the following packages:
---------------------------------------------------------------------------------------

from __future__: print_function
argparse
torch
from torchvision:  datasets, transforms




The architecture and paramenters for the model look as follows:
---------------------------------------------------------------------------------------

Conv2d Layer (3,8,'Padding',1)

BatchNormalization Layer

ReLU Layer

MaxPool Layer (2,'Stride',2)

Conv2d Layer (3,16,'Padding',1)

BatchNormalization Layer

ReLU Layer

MaxPool Layer (2,'Stride',2)

Conv2d Layer (3,32,'Padding',1)

BatchNormalization Layer

ReLU Layer

Fully Connected Layer (10)

Softmax Layer

Classification Layer (CrossEntropy)


Training parameters: 
---------------------------------------------------------------------------------------

ADAM optimizer
GradientDecayFactor (beta1): 0.9000
SquaredGradientDecayFactor (beta2): 0.9990
Epsilon: 10^(-8)
LearningRate: 0.01
Epochs: 10
L2-reg: 10^(-4)
MiniBatchSize: 128


Already after the first epoch an accuracy of 98% is reached on the test data.
