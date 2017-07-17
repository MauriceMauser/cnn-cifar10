<h1> Convolutional Neural Network </h1>
Classifying images of deer, dogs, cats, airplanes.. out of the <a href="https://www.cs.toronto.edu/~kriz/cifar.html>CIFAR-10</a> dataset, with a test accuracy of 76%.
<br>

<h2>Neural Network Architecture</h2>
3 Convolutional Layers (including ReLU nonlinearities and Max-Pooling), followed by Dropout regularization (50%) and 1 Fully Connected Layer, before the final (again, dropout-regularized) Fully Connected Output Layer. The AdamOptimizer updates the weights according to the Softmax Cross Entropy cost function. Weights are initialized with a truncated Gaussian, using a Standard Deviation of 0.1. (To arrive at a sensible estimate for the number of filters, I imagined and enumerated possible combinations of basic lines ("-", "|"...), curves ([0,pi/8], [pi/8,pi/4]...) and shapes for the first convolution; visualized combining them into circles, triangles.. on the second layer; and mentally counted things like faces on the third. The fully-connected layer uses 64 outputs, around 6 per label class, to account for bottom, front, top, side.. representations of the target objects. Probably a poor representation of what the model is actually doing, but I found it to be a useful mental model nonetheless: I arrived at 75% accuracy on the first try (before performing two rounds of hyperparameter tuning).)

<br>

<h2>Udacity Nanodegree</h2>
This is the second project in the <a href="https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101">Udacity Deep Learning Foundations Nanodegree Program</a>.
