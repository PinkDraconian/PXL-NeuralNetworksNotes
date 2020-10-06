---
title: Week 3 - Enhancements & Intro to Computer Vision
created: '2020-10-06T17:04:28.087Z'
modified: '2020-10-06T18:18:26.419Z'
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
- RMSProp
  - Automatically adjusting learning rate
- Adam
  - Combination of momentum and RMSProp

## Regularization
- Under and over fitting
- Occam's Razor
  - Simple models > Complex models
- Weight Decay
  - Weight penalty
- Early Stopping
- Dropout
- Data augmentation

## Optimization vs regularization
- Regularization
  - Reduces overfitting
  - Reducing variance without increasing bias
- Optimization
  - Focused on reducing the loss of a model
  - Centered around gradient descent

Both: Batch normalization
