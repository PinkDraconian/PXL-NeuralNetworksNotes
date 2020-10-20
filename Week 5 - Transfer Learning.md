---
title: Week 5 - Transfer Learning
created: '2020-10-20T19:02:21.188Z'
modified: '2020-10-20T19:15:43.836Z'
---

# Week 5 - Transfer Learning
## Deep learning is data hungry
Their performance is strongly correlated with the amount of available training data
## Famous CNN
- AlexNet
  + 11x11 filter, stride 4
- VGG
  + 3x3 filter, stride of 1
  + Three ReLU units
  + Fewer parameters
- GoogLeNet
  + Inception
- Residual Networks
  + Network x with 90% efficiency, network y(x) won't have at least 90% efficiency
  + Identity and Projection shortcut
- DenseNet
  + Resnet but with concatenation instead of addition

## 1x1 convolution
- Reduce number of channels (Too many feature maps)

## CNN: Inception
Deciding a fixed kernel size it difficult, how can we scale up without increasing computational costs?
Go wider. Multiple kernels of different sizes are implemented in the same layer

## CNN: Identity and Projection shortcut
Identity: Adding input with result
Projection: Adding 1x1 conv result with result

## Transfer learning
Use outputs of one or more layers of a network trained on a different task as generic feature detectors. Train a new shallow model on these features.

## Transfer learning: freeze or fine-tune
- Freeze: Don't update during backprop, do when task labels are scarce and want to avoid overfitting
- Fine-tune: Update during backprop, do when target task labels are more plentiful
