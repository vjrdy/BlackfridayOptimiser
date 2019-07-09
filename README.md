# BlackfridayOptimiser


Course Resolution
In Optimisation systems, The dataset here is a sample of the transactions made in a retail store. The store wants to know better the customer purchase behaviour against different products. Specifically, here the problem is a regression problem where we are trying to predict the dependent variable (the amount of purchase) with the help of the information contained in the other variables.
 
Resolution 1: The gradient descent
The simplest way to optimise is by calculating gradient descent is used for linear regression is the computational complexity: it's computationally cheaper (faster) to find the solution using the gradient descent in some cases.
 
. It consists in initializing the estimated matrices randomly, compute their difference to the real data, and follow the gradient of the values to reach a minimum.
The goal here is to minimize the reconstruction error. The first step is to compute this error.

Resolution 2 : Stochastic Gradient descent
Stochastic Gradient descent is a simple variant of classical gradient descent where the stochasticity comes from employing a random subset of the measurements (mini-batch) to compute the gradient at each descent. It also has implicit regularisation effects, making it suited for highly non-convex loss functions, such as those entailed in training deep networks for classification. 
Two key benefits of Stochastic Gradient Descent are efficiency and the ease of implementation. In a situation when data is less, classifiers in the module are scaled to problems with more than 10^5 training examples and more than 10^5 features.

The disadvantages of SGD include:
SGD requires a number of hyperparameters and a number of iterations
It is also sensitive to feature scaling
A compromise between computing the true gradient and the gradient at a single example is to compute the gradient against more than one training example (called a "mini-batch") at each step. This can perform significantly better than "true" stochastic gradient descent described, because the code can make use of vectorization libraries rather than computing each step separately. It may also result in smoother convergence, as the gradient computed at each step is averaged over more training examples.
Resolution 3: Mini Batch Gradient descent
 
Mini-batch gradient descent is variation of the gradient descent algorithm that splits the training dataset into small batches that are used to calculate model error and update model coefficients. Implementations may choose to sum the gradient over the mini-batch which further reduces the variance of the gradient.
Mini-batch gradient descent seeks to find a balance between the robustness of stochastic gradient descent and the efficiency of batch gradient descent. It is the most common implementation of gradient descent used in the field of deep learning.
Upsides
The model update frequency is higher than batch gradient descent which allows for a more robust convergence, avoiding local minima.
The batched updates provide a computationally more efficient process than stochastic gradient descent.
The batching allows both the efficiency of not having all training data in memory and algorithm implementations.
Downsides
Mini-batch requires the configuration of an additional “mini-batch size” hyperparameter for the learning algorithm.
Error information must be accumulated across mini-batches of training examples like batch gradient descent.




