---
layout: post
title: 'How to win data science competition: learn from top kaggler - Week 1'
---
## WEEK 1

- Introduction
- ML recap
- Hardware/Software
- pandas
- Feature preprocessing 
  - Scaling 
  - Outlier
  - Log transform, square root, ...
  - Encoding: Label encoding, frequence encoding, one hot encoding, 
  - Date time: periodicity (day of week, day of month, ...); time since (time passed after last holiday, ...); difference between dates.
  - Coordinates: clustering the coordinates; additional data (the coordinates in dataset nearby some places in the map?); aggregate stats (additional information about the areas in dataset: standard of living, ...)
  - Handle missing values: 
    - fillna approach (-999, -1, / mean, median / reconstruct values); 
    - add 'isnull' feautures. Can consider outliers as missing values. 
    - Avoid filling nans before feature generation because it can reduce the usefulness of the feature.
- Feature generation: 
  - prior knowledge
  - EDA
- Feature extraction from text: 
  - Text preprocessing: 
    - lower case
    - lemmatization: democracy, democratic, democratization ---> democracy
    - Stemming: democracy, democratic, democratization ---> democra
    - Stopwords: NLTK lib, sklearn lib (sklearn.feature_extraction.text.CountVectorizer() with max_df -max word frequence- parameter)
  - Bag of word (text -> vector): 
    - count number of words (sklearn.feature_extraction.text.CountVectorizer()); 
    - TFiDF: sklearn.feature_extraction.text.TfidfVectorizer()
    - N-gram: sklearn.feature_extraction.text.CountVectorizer(), params: Ngram_range, analyzer.
    - <u>Pipeline</u>: 
      1. preprocessing: lower case, lemmatization, stemming, stopwords
      2. Ngram (optinal)
      3. Postprocessing: TFiDF
  - Word2vec, CNN: 
    - Word-based library: Word2vec, Glove, FastText, ...
    - Sentence-based library: Doc2vec
    - There are pretrained models.
- Feature extraction from image:
  - CNN, pretrained model.
