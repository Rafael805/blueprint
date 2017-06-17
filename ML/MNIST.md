# MNIST for ML Beginners (softmax regression)

Every MNIST data point has two parts: an image of a handwritten digit and a corresponding label. The images "x" and the labels "y". Both the training set and test set contain images and their corresponding labels; for example the training images are ```mnist.train.images``` and the training labels are ```mnist.train.labels```.

These two lines of code will download and read in the data automatically:

```
from tensorflow.examples.tutorials.mnist import input_data
mnist = input_data.read_data_sets("MNIST_data/", one_hot=True)
```

The MNIST data is split into three parts: 55,000 data points of training data (```mnist.train```), 10,000 points of test data (```mnist.test```), and 5,000 points of validation data (```mnist.validation```). This split is very important:

it's essential in machine learning that we have separate data which we don't learn from so that we can make sure that what we've learned actually generalized.
 
```mnist.train.images``` is a tensor (n-dimensional array) with a shape of ```[55000, 784]```
 
The first dimension is an index into the list of images and the second dimension is the index for each pixel in each image. Each image is 28 pixels by 28 pixels = 784

Each image in MNIST has a corresponding label, a number between 0 and 9 representing the digit drawn in the image.

# Softmax Regressions
Every image in MNIST is of a handwritten digit between zero and nine. So there are only ten possible things that a given image can be. We want to be able to look at an image and give the probabilities for it being each digit. For example, our model might look at a picture of a nine and be 80% sure it's a nine, but give a 5% chance to it being an eight (because of the top loop) and a bit of probability to all the others because it isn't 100% sure.

If you want to assign probabilities to an object being one of several different things, softmax is the thing to do, because softmax gives us a list of values between 0 and 1 that add up to 1. Even when we train more sophisticated models, the final step will be a layer of softmax.

A softmax regression has two steps:   
1. Add up the evidence of our input being in certain classes 
2. Convert that evidence into probabilities

To tally up the evidence that a given image is in a particular class, we do a **weighted sum** of the pixel intensities. The weight is negative if that pixel having a high intensity is evidence against the image being in that class, and positive if it is evidence in favor.

We also add some extra evidence called a **bias**. Basically, we want to be able to say that some things are more likely independent of the input.


