### What is a logistic classifier?

A logistic classifier is what's called the *linear classifier*. It takes input, for example pixels in an image, and applies a linear function to them to generate its predictions. A linear function is just a giant matric multiplier. 
![classifier](https://github.com/Rafael805/blueprint/blob/master/ML/logistic%20classifier.png)

It takes all the inputs as a big vector that will "X" and multiplies them with a matric to generate its predictions, one per output class.  

X: inputs  
Weights: W  
Bias term: b  

The weights of that matrix and the bias is where the machine learning comes in. The model needs to be trained. That means we need to find the values for weights and bias which are good at performing these predictions.

Each image that we have as an input can have only one possible lable. We need to turn those scores into probabilities. We want the probablity of the correct class to be very close to 1 and the probablity for every other class to be close to 0. The way to turn scores into probabilities is to use a softmax function. It can take any kind of scores and turn them into proper probabilities. Scores in logistic regression are often called logits scores. 

![scores](https://github.com/Rafael805/blueprint/blob/master/ML/logistic%20classifier.png)
