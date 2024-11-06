# Questions

This document provides the group's answers to the questions proposed in the assignment.

1. Plot the training and validation error and accuracy metrics.

*See the last code block in the* 'neural_network_A3.ipynb' *Jupyter Notebook for validation error*
*and accuracy metrics*.

2. What hyperparameters did you use to tune your model and why? For example, the number of hidden
layers, number of neurons, activation function, input features, etc.

We tested various hyperparameters to tune our model.

For the input layer we used an input layer with 28 * 28 = 784 features. This was because the images
consisted of 28 * 28 pixels each. We also included a flatten layer in our layer architecture.

We used two hidden layers, where one layer was a convolution layer with 32 neurons, and the other
was a dense layer with 96 neurons. Both layers used ReLU as acitivation function. We saw that as we
increased the neurons in the dense layer the training accuracy increased as well. Thus, we wanted
to keep this layers with a high number of neurons, but not too high to avoid overfitting our model.
We also added a dropout layer to avoid this.

When adding the output layer we used a dense layer with softmax as activiation function. This layer
used 10 neurons, as our classification problem had 10 classes.

When compiling the model we first tried using *sgd* as optimizer, but did not get a training
accuracy we were satisfied with. We did some research and found that the *adam* optimizer might fit
our model. We then tried using this optimizer instead and got a better accuracy. For our loss
function we used *sparse categorical crossentropy* as our model had to do with a classification
problem.

Lastly, we used 10 epochs when training our neural network. For this, we tried a few different
amounts, and quicly discovered that our model was overfitting when using too many epochs.

The final training accuracy was 91.28 % while the loss was 23.45 %.
