# Sentiment-Analysis-of-Amazon-Reviews
In this project a Neural Network model based on Recurrent Neural Networks aims to predict whether review on Amazon conveys a positive or a negative sentiment. For each review the model predicts a value between 0 and 1 for conveying a particular sentiment where 1 means absolute positive and 0 implies absolute negative.

In case of Recurrent Neural Network I am using Gated Recurrent Units(GRU's) networks.To get a good result on the sentiment of review, pretrained BERT model is used for obtaining the embedding for words . Also overfitting is prevented by using dropout.
## Getting Started
Pytorch 

Transformers

## Data
Dataset was taken from kaggle (link : https://www.kaggle.com/marklvl/sentiment-labelled-sentences-data-set).
The dataset contains reviews and scores for products sold on amazon.com in the cell phones and accessories category,and is part of the dataset collected by McAuley and Leskovec.There exist 500 positive and 500 negative sentences.
The reviews are preprocessed by specifying the pipeline in pytorch Field and Label.
## Model
The model is a Neural Network with the following layers:
1. Embedding layer which uses pretrained bert-base-uncased (To get good accuracy without training over large dataset)
2. Bi-GRU RNN with 0.25 dropout 
3. Fully connected output layer

The model gives the test accuracy of 91.02%
