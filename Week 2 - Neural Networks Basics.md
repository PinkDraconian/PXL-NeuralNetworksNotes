---
title: Week 2 - Neural Networks Basics
created: '2020-09-29T11:08:51.182Z'
modified: '2020-09-30T15:02:57.713Z'
---

# Week 2 - Neural Networks Basics
## Shallow vs deep NN
1 hidden layer vs more hidden layers

## Input and output data
- Input
  - Images (RGB or grayscale of every pixel)
  - Tabular data
    - Label encoding
    - One hot encoding
    - Categorical embeddings
- Output
  - Regression: 1 or more values
  - Classification: One output neuron per class, using softmax get a probability

## Forward propagation
Inputs -> Weights -> Summation and bias -> Activation -> Output
- Summation and bias: $\sum_{i=1}^m(w_ix_i) + bias$

## Activation function
- Sigmoid
  - Logistic activation function
  - Results between 0 and 1
  - $\phi(z) = \frac{1}{1 + e^{-z}}$
- Tanh
  - Hyperbolic tangent activation function
  - Results between -1 and 1
- ReLU
  - Rectified Linear Unit
  - Results between 0 and $z$
  - $R(z) = max(0, z)$
  - Easy to calculate
  - Nodes arriving at large negative values  (due to unfortunate random initialization, too large learning rate, high bias numbers) will be set to 0, won't be activated and won't be able to recover from this, thus effectively killing the node.
- Leaky ReLu
  - $f(x) = \begin{cases} 0.01x, & \text{if}\ x < 0 \\ x, & \text{otherwise} \\ \end{cases}$
- ELU
  - Exponential Linear Unit
  - Kleiner dan 0: $\alpha(e^x-1)$
  - Domain between -1 and inf

## Cost function
- Regression problem
  - Mean squared error: $MSE = \frac{1}{n}\sum_{t=1}^{n}e_t^2$
  - Root mean aquared error: $RMSE = \sqrt{\frac{1}{n}\sum_{t=1}^{n}e_t^2}$
  - Mean absolute error: $MAE = \frac{1}{n}\sum_{t=1}^{n}|e_t|$
- Classification problem
  - Cross-entropy loss: $L_i = - \sum_ky_klog(S(l_k))$
    - The negative of the sum of the resulting label times the logarithm of the calculated probability. 

## Minimizing loss / Adjusting weights
$w = w - \alpha\frac{\theta loss}{\theta w}$ with $\alpha$ as the learning rate and $\frac{\theta loss}{\theta w}$ as the gradient

- Vanishing gradient problem
For certain activation functions (Sigmoid), big changes in the input, cause small changes in the derivative and thus the gradient might get too small to effectively train
