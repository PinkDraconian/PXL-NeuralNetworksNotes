---
title: Questions and Answers
created: '2020-09-25T07:45:26.116Z'
modified: '2020-09-25T07:55:26.243Z'
---

# Questions and Answers
## Week 1
### Bespreek de "goodness" van een model tijdens training, en tijdens test fase. Voor zowel classification als regression.
Kijken of de prediction realistisch is en accuraatheid onderzoeken

Stappenplan:
1. dataset dubbelchecken/cleanen 
2. dataset vergroten of verkleinen 
3. hyperparameters toepassen (tijdens testfase)
4. batches
5. variance verminderen

Overfit --> train goed test slecht --> stoppen met trainen/verkeerde features/meer data/Random forest ipv single (meer ongecontroleerde trees)
Underfit --> train slecht test slecht

### Wat is het probleem met een unbalanced dataset. Hoe kan oversampling of undersampling dit oplossen? Wordt deze techniek bij DL ook toegepast?
- Oversampling meestal goed --> verschillende categorieen beter herkennen
- Collect more data from the minority class
- Use penalized models
- More: https://medium.com/strands-tech-corner/unbalanced-datasets-what-to-do-144e0552d9cd
