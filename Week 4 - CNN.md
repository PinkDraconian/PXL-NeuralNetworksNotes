---
title: Week 4 - CNN
created: '2020-10-13T16:06:23.155Z'
modified: '2020-10-13T16:26:15.388Z'
---

# Week 4 - CNN
## Motivation for CNNs
- Images are big
  + Too many parameters for feed forward networks
- Positions can change

## Problems with convolutions
- Image shrinks
  + Add padding
  + $output\_size = \frac{n + 2p -f}{s} + 1$
    - n = input size
    - p = padding size
    - s = stride (How many pixels the filter moves )
    - f = kernel size

## Convolution block
Conv2D -> BatchNorm -> ReLU -> MaxPool

## Image classification vs detection
Classification: Traditional CNN
Classfication with localization: Simplified YOLO, R-CNN
Detection: YOLO, R-CNN
