# BiLSTM-CRF-FastAPI
This respository include the code for building a Malay POS tagger by using Bi-LSTM-CRF.
The dataset is small. To overcome overfitting, pre-trained word embedding is used.
The model is then deploy by FastAPI.

## Requirement
**ALL the code run in Google Colab.**
### Python Library
Gensim -to train Word2Vec embedding matrix

tensorflow version 1.13.1 

keras version 2.2.4 

keras contrib - extension for Keras. CRF layer need this library

*save and load model need a bit more work as the extension of Keras layer. refer https://github.com/keras-team/keras-contrib*

## Dataset
the dataset is in the form of : 

pengulas/KN pun/KPN macam/KN tak/KNF-KEP tahu/KA apa/GDT-KTY nak/KB-KEP juga/KPN ni/GT-KEP

## Files

### word2vec
code for generate embedding matrix of the dataset with the help of Python library Gensim

### train model
code for data pre-processing, model building and model trainning

*Since the dataset used is small, to overcome overfitting, i combined the matrix (trained from my dataset) and the pre-trained embedding matrix from Kyubyong (https://github.com/Kyubyong/wordvectors), which is trained from bigger dataset.*

### index_to_tag.pickle and word_to_index.pickle
This pickle file contained the index for each word and tag that converted in the train_model.ipynb

### best model
code for testing the best model that give good fit

### FastAPI
code for generate the API for user to use the system

## Result

![image](https://user-images.githubusercontent.com/82029895/127024289-1184262c-b22e-4fc9-a12b-e3764ed2c103.png)

