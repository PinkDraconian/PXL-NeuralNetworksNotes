---
title: Week 7 - NLP
created: '2020-11-14T09:16:54.460Z'
modified: '2020-11-14T09:40:17.032Z'
---

# Week 7 - NLP
## NLP Language is hard
- Reference resolution (Wat slaat op wat?)
- Lexical ambiguity (Een woord betekend in context andere dingen)
- Syntactic ambiguity (Visiting relatives can cause problems)
- Irony and sarcasm
- Subjectivity of annotations

## NLP 2 prevailing cultures in linguistics
- Strong AI: Modeling the underlying mechanism
- Weak AI: Predicting output without necessarily understand the mechanism behind it

## NLP Use cases
- Information retrieval
- Sentiment analysis
- Information extraction
- Machine translation
- Question answering

## Classical vs deep NLP
- All docs at once as one huge matrix with numbers input
- Each record on at a time as input

## Wordnet problems
- Misses nuances and context
- Misses new words
- Human-made (Labor intensive)

## Language Model
Model that understand the given language
- Relations between words
- Basis for classification, translation, predicting

## Text Preprocessing
Level of preprocessing needed:
- Little data and noisy texts: LOTS
- Lots of data and well written: LITTLE
### Tokenization
- N-grams: splitting text up depending on n (n words at a time)
### Token normalization
- Stemming: bring word to simpler form
- Lemmatization: bring word back to root form
- Stop word removal
- Capital letters
- Acronyms
- Noise removal
### Vectorization
- Frequency based
  + Bag of words (One hot encoding)
  + TF-IDF: Occurences / Total terms * log(ratio of docs that use word), Causes words occuring everywhere to be 0
  + hashing tables
- Probability based
  + Word2Vec: Dependency structure, word is represented by context in use
    - CBOW: Predict middle word based on context
    - Skip-Gram: Use word to predict context
  + GLoVe
  + FastText
