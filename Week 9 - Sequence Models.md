---
title: Week 9 - Sequence Models
created: '2020-11-25T10:07:35.590Z'
modified: '2020-11-25T10:15:48.516Z'
---

# Week 9 - Sequence Models
## RNN Use cases
- Sequence prediction
- Sequence classification
- Sequence generation
- Sequence-to-sequence prediction

## RNN problems
- Vanishing gradients (Weight changes becomes small through time (No long term memory))

## LSTM Process
- Forget irrelevant parts of previous state (Sigmoid)
- Selectively update cell state values (Sig + tanh)
- Output certain parts of cell state
