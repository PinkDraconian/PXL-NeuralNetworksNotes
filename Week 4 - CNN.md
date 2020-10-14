---
title: Week 4 - CNN
created: '2020-10-13T16:06:23.155Z'
modified: '2020-10-14T20:10:53.280Z'
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

## Questions
### Waarom gebruiken we geen DNN om computer vision te doen op images?
1. anders zijn er veel te veel input parameters. elke image heeft een r, g, b en alpha
2. als de image verspringt is het minder gegeneraliseerd. als objecten op verschillende locaties staan

### Leg een typisch CNN architectuur uit voor image classification
1. Padding
2. Convolution layer
3. Batch normalisation
4. Activation
5. Pooling
6. Flattening
7. Dense layer
