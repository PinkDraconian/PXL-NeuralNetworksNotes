---
title: Week 3 - Enhancements & Intro to Computer Vision
created: '2020-10-06T17:04:28.087Z'
modified: '2020-10-06T19:47:39.791Z'
---

# Week 3 - Enhancements & Intro to Computer Vision

## Computer Vision
### ImageNet
Large database of hand categorized images, which can be used to benchmark models against

### Tensors
Images can be represented as a 3D-matrix
Lists of images as a 4D-matrix

## Initialization
- Initialize weights randomly
  - Vanishing or exploding gradients
- Xavier
  - GlorotNormal / GlorotUniform
  - Best for Sigmoid or Tanh activation functions
- He
  - Normal / Uniform
  - Truncated normal distribution
  - Best for ReLU activation functions

## Optimization
- Stochastic Gradient Descent
  - Complex loss landscapes
  - Saddle points
  - Pathological curvature (Rondspringen in een dal), can slow down training because the gradient will keep on bouncing off walls
- (Mini) Batch size
- Learning rate
  - Too small requires too many updates before reaching minimum
  - Too large causes drastic updates leading to divergent behaviors
- Cycling learning rates
- Momentum
  - Accumulate the gradient of the past steps
  - Fights against pathological curvature due to the cancellation of the vector in that axis
- RMSProp
  - Automatically adjusting learning rate
- Adam
  - Combination of momentum and RMSProp

## Regularization
Encourages models to have a preference towards simpler models

- Under and over fitting
- Occam's Razor
  - Simple models > Complex models
- Weight Decay
  - Weight penalty (Penalizes large weights)
  - $Loss <- Loss + (Weight penalty)$
  - L1 Regularization (LASSO)
    - Weight penalty = $\alpha \sum_i |w_i|$ with $\alpha$ being the regularization strength
    - Sparser weights
  - L2 Regularization
    - Weight penalty = $\alpha \sum_i w^2_i$ with $\alpha$ being the regularization strength
    - Smaller weights

- Early Stopping
  - Initialize with small weights and stop when model stops improving
- Dropout
  - Encourages neuron to learn without relying on other neurons
  - When using the model, all neurons are used
  - Similar to ensemle methods, where we train multiple neural networks and combine them
    - The difference is that with dropout, the models aren't disjoint.
- Data augmentation
  - Creates more data
  - Rotating, mirroring, noise, contrast, ...

## Optimization vs regularization
- Regularization
  - Reduces overfitting
  - Reducing variance without increasing bias
- Optimization
  - Focused on reducing the loss of a model
  - Centered around gradient descent

Both: Batch normalization
