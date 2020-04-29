#Twitter Sentiment Analysis

The data set used for this analysis is downloaded from kaggle using this [link](https://www.kaggle.com/kazanova/sentiment140).


## Overview:

This is a simple attempt to classify the sentiment of some tweets using SVM and a simple shallow Neural Network.

The size of the data set is around 1600000 entry, but for this training we have used only 10000 randomly chosen tweets to work on.

## Libraries used

* spacy
* nltk
* sklearn.svm
* pytorch (for neural net)

## Preprocess

The text was preprocessed using the following steps:

* Remove Hashtags
* Remove Mentions
* Expand contractions using hardcoded mappings
* Remove stop words based on nltk corpus stopwords
* Remove Emails
* Remove URLs
* Remove Special Characters
* Remove Multiple spaces
* Remove Punctuations
* Tokenize
* Transform into word embeddings using spacy library


## Training


First, a model was trained using a linear SVM imported from sklearn. Then, we used the same data to train a 3-layer neural network with a sigmoid output node.


## Outcomes

Due to relatively small size of the data the accuracies resulting from the SVM and neural net respectively were 0.73 and 0.694 using a test set randomly sampled as 10% of the original data.
