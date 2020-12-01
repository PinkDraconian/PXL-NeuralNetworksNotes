---
title: Week 10 - Unsupervised Deep Learning
created: '2020-12-01T20:06:52.825Z'
modified: '2020-12-01T20:14:23.452Z'
---

# Week 10 - Unsupervised Deep Learning
## LeCake
- RL: Cherry on cake
- Supervised Learning: Icing
- Unsupervised: Cake

## Problems with supervised learning
- Labels introduce human bias
- Labeling not cost effective
- Too much domain knowledge needed
- Humans don't learn like this

## Types of unsupervised learning
- Non-probabilistic (Self-supervised)
- Probabilistic (Generative)

## Autoencoders
Take image and try to reproduce image using latent space (pacman)
Encoder > Bottleneck < Decoder

## Autoencoders L1 vs L2 loss
Mae vs mse
crispy vs blurry image

## Use cases autoencoders
- Anomaly detection
- Denoising
- Pretraining (Semi supervised)
- Similarity detection
- Generative modeling

## Generative Adversarial Networks
Generator -> Discriminator -> Loss Function
Generate fake image, discriminate will say whether fake or not and then the generator will want to maximize loss, discriminator, minimize
