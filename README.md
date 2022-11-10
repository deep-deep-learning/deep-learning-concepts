# Machine Learning / Deep Learning Concepts

### Optimizers

- Gradient Descent
    - new_variables = old_variables - learning_rate * the gradient of old_variables to loss function.
    - Follows gradient to optimize the variables.
- Stochastic Gradient Descent
    - Uses mini-batch to update instead of full batch from gradient descent.
    - Highly affected by learning_rate and batch_size.
- Momentum
    - Adds a momentum (proportional to last velocity) to gradient to compute velocity.
    - Helps to move away from local minima (i.e. when gradient is 0).
- RMSProp
    - Divides gradient by sqrt(avgerage gradient squared) to learn more from the less learned parameters and learn less from the more learned parameters.
    - Adaptive learning rate for each parameter.
- Adam
    - Momentum + RMSProp


### Activation Functions

- Sigmoid
    - Suffers from vanishing gradient at the tail portion of the function.
    - Therefore, slow to converge.
- Tanh
    - Like zero centered sigmoid.
    - Still suffers from the vanishing gradient problem.
- ReLU
    - y = max(0, x).
    - Solves vanishing gradient problem.

### Regularization

- L1
    - Adds abs(W) to the loss function.
    - Induces sparsity.

- L2
    - Adds root square of W to the loss function.
    - Better when all features are meaningful.
    - Differentiable thus optimizable with gradient approaches.

- Dropout
    - Every training epoch, randomly selects neurons and sets activation to 0.
    - Like learning an ensemble of subnetworks.

- Early stopping
    - Prevents overfitting by stopping training when test loss stops improving.