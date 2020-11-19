---
title: Week 8 - NLP
created: '2020-11-19T17:30:41.039Z'
modified: '2020-11-19T18:05:31.492Z'
---

# Week 8 - NLP
## ULMFiT
Transfer learning technique which can help in various NLP tasks
- General-Domain LM Pretraining; pretraining on large corpus
- Target Task LM Fine-Tuning; fine-tuning on dataset for target task
- Target Task Classifier; ReLU and softmax to get probabilities

## SL, BS, BPTT in LM
1. Get lot of docs
2. Extract text, preprocess and numericalize
3. Concat docs
4. Subdivide in chunks of SL items
5. Stack BS sequences
6. Take slices of BPTT length for x and move 1 along for y

## ELMo
vector assigned to a token or word is actually a function of the entire sentence (context) since the same word can have different word vectors under different contexts.

## BERT
Relies on transformers and masks words in sentences to guess them.
1. Semi-supervised training on large corpus
2. Supervised training on labeled dataset for specific task

## NLP Learning tasks
- One to one
- One to many (Sequence output)
- Many to one (Sentiment analysis)
- Many to Many (Sequence in and output)

## RNN
Process text in sequential order
### Problems
- Long term dependencies
- Don't ignore unimportant info
- Vanishing gradients
- Copy of copy (Lose quality)


## Seq2Seq
Encoder RNN -> Decoder RNN

## Attention
- Self-Attention
  + Learns which parts of text are most important in order to better encode

## Transformer
- Uses attention in seq2seq context
- Not sequential, no RNNs
- More parallellization
