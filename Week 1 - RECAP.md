---
attachments: [Clipboard_2020-09-21-19-52-19.png]
title: Week 1 - RECAP
created: '2020-09-21T16:58:14.081Z'
modified: '2020-10-07T08:28:04.909Z'
---

# Week 1 - RECAP
## Setting the scene
- Artificial Intelligence (AI) - 1950s - Any technique that enables machines to mimic human behaviour
- Machine Learning (ML) - 1980s - Subset of AI which uses statistical methods to learn without being explicitly programmed
- Deep Learning (DL) - 2010s - Subset of ML in which multilayered neural networks learn from large amounts of data

## Base conditions
1. GPU > CPU
2. Big Data storage
3. Base algorithms in the cloud

## Data driven
Datasets over algorithms

## Algorithms
- Supervised
  - Labeled data
  - Direct feedback
  - Predict outcome / future
- Unsupervised
  - No labels
  - No feedback
  - "Find hidden structure"
- Reinforcement
  - Decision process
  - Reward system
  - Learn series of actions

## Types of problems
- Regression
- Classification
- Dimensionality reduction (PCA)
- Clustering (kNN) -> Data mining and knowledge discovery
- Recommendation systems
- Anomaly detection

## Parameters
- Hyperparameters - Part of model design
- Parameters - Trainable

## Goodness of a model
- Mean Square Error (MSE)
- Loss function
- Confusion Matrix
  | | Guessed Positive | Guessed Negative |
  | --- | --- | --- | 
  | **Positive** | True Positives | False Negatives |
  | **Negative** | False Positives | False Negatives |
  - $accuracy = (True Positives + True Negatives) / Total Points$
  - $precision = True Positives / (True Positives + False Positives)$
  - $recall = True Positives / (True Positives + False Negatives)$
- Over and under-fitting
- Bias vs. Variance
  - High bias - Little attention to data | Oversimplified | High error on training set
  - High variance - Too much attention to data | Overfits | High error on test set
  ![](@attachment/Clipboard_2020-09-21-19-52-19.png)
- Inaccurate labels
- Missing data
- Unbalanced data sets (100 cat pictures, 1 million dog pictures)

## Feature selection
- Common sense
- Independent features (Use correlation heatmap)
- Determine effective features (Trial and error (Pruning))

## Epoch - Batch - Iteration
- Epoch - An Epoch represents one iteration over the entire dataset
- Batch - We cannot pass the entire dataset into the neural network at once. So we divide the dataset into number of batches.
- Iteration - If we have 10000 images as data and a batch size of 200, then one epoch should contain 50 iterations

## Bespreek de "goodness" van een model tijdens training, en tijdens test fase. Voor zowel classification als regression.
Kijken of de prediction realistisch is en accuraatheid onderzoeken

Stappenplan:
1. dataset dubbelchecken/cleanen 
2. dataset vergroten of verkleinen 
3. hyperparameters toepassen (tijdens testfase)
4. batches
5. variance verminderen

Overfit --> train goed test slecht --> stoppen met trainen/verkeerde features/meer data/Random forest ipv single (meer ongecontroleerde trees)
Underfit --> train slecht test slecht

## Wat is het probleem met een unbalanced dataset. Hoe kan oversampling of undersampling dit oplossen? Wordt deze techniek bij DL ook toegepast?
- Oversampling meestal goed --> verschillende categorieen beter herkennen
- Collect more data from the minority class
- Use penalized models
- More: https://medium.com/strands-tech-corner/unbalanced-datasets-what-to-do-144e0552d9cd
