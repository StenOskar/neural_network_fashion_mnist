# Questions

This document provides the group's answers to the questions proposed in the assignment.

1. Plot the training and validation error and accuracy metrics.

Our best accuracy was 0.9251% and our best loss was 0.2008. The model was trained for 10 epochs.

2. What hyperparameters did you use to tune your model and why? For example, the number of hidden
layers, number of neurons, activation function, input features, etc.

To tune the model we used two convolution layers with 32 and 64 filters, and a dense layer with 128 neurons.
We used Relu as the activation function. Our output layer has 10 neurons. we also implemented a dropout layer
with a value of 0.5 to prevent overfitting.
The use of Adam optimizer helped the algorithm to minimize the loss function during training.
To increase the accuracy of the model. We added a second convolution layer to the model. which took the
accuracy from 0.8993% to 0.9251%.
