This is Python notebook that implements a neural network for MNIST from scratch, utilizing only numpy. The main requirements are having the proper packages installed and downloading the train and test images/labels for MNIST (done automatically through downloading python-mnist) (or whichever other dataset you want to use). Make sure the data is stored as a numpy array.
The only package you would need is numpy. If you would like to use MNIST, also install python-mnist and mlxtend. If you want to see training progress, install tqdm. If you want to visualize data, install matplotlib. For implementation in Google Colab, only python-mnist needs to be installed.

The code is situated as such:
1. All the necessary imports.
2. Loading in data and basic preprocessing.
3. Creation of necessary functions and classes. The way I implemented the model is by first creating a Layer class that includes regularization, activation, and forward/backward passes. There is then a Network class which contains a list of Layers, and can pass data through multiple layers in order and also backpropagates through layers. It also contains the loss function used. The network class also includes a method to train its model, with many options inside of that (batch size, early stopping, verbose, etc.). It also has methods to evaluate model performance.
4. Example of training a model.
5. Implementation of my network as an autoencoder for the MNIST dataset.

The supported activation functions ReLU, sigmoid, tanh, and softmax. Note that softmax must be paired with cross-entropy loss and should only be used on the last layer. The supported regularization is L2 Regularization, with dropout on its way. The supported loss functions are MSE and cross-entropy. Note that cross-entropy must be paired with the softmax activation function in the last layer.

