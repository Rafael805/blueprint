# What is backpropagation?

Backpropagation is the key algorithm that makes training deep models computationally tractable. For modern neural networks, it can make training with gradient descent as much as ten million times faster, relative to a naive implementation. That’s the difference between a model taking a week to train and taking 200,000 years. The general, application independent, name is “reverse-mode differentiation.” Fundamentally, it’s a technique for calculating derivatives quickly. 
