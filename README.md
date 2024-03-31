# Natural Language Processing with Disaster Tweets
## Project Overview
This project is an introduction to Natural Language Processing on Kaggle. You can find the full description of the project, as well as the dataset on the official Kaggle page: [NLP Getting Started Competition.](https://www.kaggle.com/competitions/nlp-getting-started)

The goal of the project is to predict whether a tweet is about a disaster or not. This could be very useful to help emergency services react quickly in case of a disaster.

## My Approach
I started by analyzing the dataset and decided not to use the localization and keyword features of the dataset. Indeed, the localization did not provide much useful information to discriminate between disasters and non-disasters.

Then, I cleaned my dataset by removing stopwords, stemming the words, and tokenizing the tweets. I also created a vocabulary by removing words that only appeared once in the dataset.

I used a deep learning approach using PyTorch. I started by creating an Embedding layer and then tried a few model architectures:

Model 1: RNN with L2 regularization (weight_decay=0.01)
Model 2: RNN with a dense layer of 16 neurons without regularization
Model 3: LSTM without regularization
Model 4: LSTM with L2 regularization (weight_decay=0.01)
Model 5: LSTM with L2 regularization (weight_decay=0.02)
After analyzing the learning curves (Loss, Accuracy, and F1 Score), I decided to use Model 4 and stopped the training after 18 epochs.

## My Results on Kaggle
I submitted my predictions on Kaggle on March 31st, 2024, and I received a score of 0.78179.