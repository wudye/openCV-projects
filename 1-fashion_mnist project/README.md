Fashion MNIST is a popular machine learning dataset and serves as an alternative to the classic MNIST handwritten digit dataset. This case uses cross-entropy loss function to measure the error between true values and predicted output values, while the Adam optimizer applies the error calculated by the loss function to the trainable parameters within the neural network through backpropagation.

Backpropagation
Error Calculation: First, calculate the gap between the model's predicted output and the true target in the current iteration. This is typically transformed into a calculation of a loss function (such as cross-entropy, mean squared error, etc.).

Gradient Calculation: Using the chain rule, start from the output layer and calculate the gradient of each intermediate variable and parameter with respect to the total loss function layer by layer in reverse order. In other words, calculate the derivative of the loss with respect to the weights and biases of each layer in the network.

Parameter Update: Based on the calculated gradients, use optimization algorithms (such as gradient descent, momentum, Adam, etc.) to update the network's weights and biases. The update direction is opposite to the gradient direction, with the goal of reducing the value of the loss function.

Cross-Entropy Loss Function
Cross-Entropy Loss is one of the most commonly used classification loss functions in deep learning.

Basic Concepts
Cross-entropy is used to measure the difference between two probability distributions. In classification tasks:

Predicted Distribution: The probability output by the model (after Softmax activation)
True Distribution: The actual labels (one-hot encoded)
sparse_categorical_crossentropy: Used when labels are integers (0-9)
categorical_crossentropy: Used when labels are one-hot encoded
Adam Algorithm
The core of the Adam algorithm lies in calculating adaptive learning rates for each parameter.

Initially, Adam initializes two vectors m and v, whose shapes are the same as the model parameters θ. The vector m is used to store the moving average of gradients, while v tracks the moving average of squared gradients. These moving averages are crucial for Adam's adaptive adjustment. A time step counter t is also initialized to zero, which tracks the number of iterations (or updates) completed by the algorithm