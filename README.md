# Twitter-Sentiment-Classifier
A twitter sentiment classifier based on Support Vector Machines algorithm

## Overview

Sentiment analysis is a field of study which identifies the opinion of people expressed in a text using natural language processing tools. Social media such as Twitter provides a constant source of textual data, many with an opinion, which can be analyzed using Sentiment Analysis tools.

The code is written in Python and uses scikit-learn library . We use Support Vector Machine (SVM) with Linear kernel.
## Classes of Sentiment

Two classes: Negative(0) and Positive(1).

## Training data

The following training data is publicly available and is collectively used for training the classifier:

#### Stanford Sentiment140
http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip Size: 1,600,000 tweets

#### Polarity Dataset v2.0
http://www.cs.cornell.edu/people/pabo/movie-review-data/ Size: 1000 positive and 1000 negative processed movie reviews

#### Univeristy of Michigan
https://inclass.kaggle.com/c/si650winter11 Size: 7086 sentences from social media (not necessarily twitter)

## Preprocessing the tweet

We have applied a set of pre-processing steps to make tweets suitable for SVM algorithm and improve performance. The following pre-processing has been done on the tweets:

i. Lower Case - Convert the tweets to lower case

ii. URLs - Convert www.* or https?://* to 'URL'

iii. @username - Convert username to '__HANDLE'

iv. #hashtag - Hash tags can give us some useful information, so we replace them with the exact same word without the hash. E.g. #Apple replaced with 'Apple'

v. Trimming the tweet

vi. Repeating words: People often use repeating characters while using colloquial language, such as "I’m exciteddddd". We replace characters repeating more than twice with just two characters, so that the result for above would be "I'm excitedd"

vii. Emoticons: Use of emoticons is prevalent in tweets. We identify a set of emoticons and replace them with the reprentative sentiment i.e. '__positive__' or '__negative__'. E.g. ':)' is replaced by '__positive__'. Further, if emoticon(s) are found in the tweet, then the SVM classifier is not called and the tweet is classified as positive or negative simply based on the emoticon.



## Required libraries

To use the classifier, you must have the following libraries installed:

i. scikit-learn version is 0.17.1. (http://scikit-learn.org/stable/install.html)

ii. NLTK version 3.2.1 (https://pypi.python.org/pypi/nltk)

iii. numpy (http://www.numpy.org/)

iv. scipy (https://www.scipy.org/)


## Output

The output of the sentiment analyzer is either 0 (Negative) or 1 (Positive). 
