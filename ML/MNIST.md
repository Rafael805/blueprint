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
