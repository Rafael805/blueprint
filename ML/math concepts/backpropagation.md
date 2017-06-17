# What is backpropagation?

Backpropagation is the key algorithm that makes training deep models computationally tractable. The expression tells us how quickly the cost changes when we change the weights and biases. It actually gives us detailed insights into how changing the weights and biases changes the overall behaviour of the network. 

For modern neural networks, it can make training with gradient descent as much as ten million times faster, relative to a naive implementation. That’s the difference between a model taking a week to train and taking 200,000 years. The general, application independent, name is “reverse-mode differentiation.” Fundamentally, it’s a technique for calculating derivatives quickly. 
