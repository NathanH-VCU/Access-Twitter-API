# CMSC 516 Twitter/YouTube Sentiment Analysis

## Content

| Section | Description |
|-|-|
| [Project description](#project_description) | Detailed description of the project |
| [Installation](#installation_instructions) | How to install the package |
| [Overview](#overview) | Overview of the package |
| [Method](#method) | Method used for codes |
| [Doc](#doc) |  Detailed documentation |
| [Notebooks](#notebooks) | Introduction on the provided Jupyter Notebooks |
| [Data](#data) | Data used to train the models |
| [Results](#results) | Results of the models |

## Project Description
Our Project utilizes the BERT model and PyTorch to provide a sentiment analysis of our YouTube Comments dataset ... to use on our twitter dataset ...

In our project, we analyze the comments of most recent YouTube videos and we evaluate whether they are positive, negative or neutral with the pre-trained model BERT.
We compare the results obtained with YouTube Comments dataset and the results obtained with YouTube Tweets.

The dataset in extracted from Kaggle website.

In order to analyze the comments, we used Pre-trained BERT model to score the sentiment (positive,negative,neutral) per comment and then averaged them per video. 

## Overview

This package comprises the following classes that can be imported in Python :

  - [`BertModel`](./pytorch_pretrained_bert/modeling.py#L639) - raw BERT Transformer model (**fully pre-trained**),
  - [`BertForSequenceClassification`](./pytorch_pretrained_bert/modeling.py#L916) - BERT Transformer with a sequence classification head on top (BERT Transformer is **pre-trained**, the sequence classification head **is only initialized and has to be trained**),
  - [`BertTokenizer.from_pretrained`](./pytorch_pretrained_bert/modeling.py#L1051) - BERT Transformer with a token classification.
- The **Transformer** PyTorch models (`torch.nn.Module`) 
- Optimizer for **BERT**  `Adam` - Bert version of Adam algorithm with warmup and linear decay of the learning rate.

## Installation Instructions
This repo was tested on Python 2.7 and 3.5+ 
This project was built abd tested in Google Colab. It can be ran the same way. To run this project yourself:
1. Follow this link to the Google Colab -
2. Go to the Colab task bar
3. Click Runtime
4. Click Run All
5. Wait until the process finishes, our tests took about _____ time.

## Usage Instructions

## Method
1. For the code for Sentiment Analysis using BERT titled : 
BERT_sentiment_analysis_using_Youtube_Comments.ipynb
-	Feature representation : Bert contextual embedding
-	Python Algorithm : Gradient Descent machine Learning algorithm
-	Dataset : YouTube comments from Kaggle

## Data
For our data we are utilizing Kaggle's YouTube Statistics dataset, specifically the ccomments.csv file. This data set contains a list of Video ID's, comments, likes, and the Sentiment of the comments. For our project we are only utilizing th comments and their sentiment for training and developing our model.
The size of our data set is 18,409 comments with 12.7% negative sentiment, 25% neutral sentiment, and 62% positive sentiment. 

## Doc

Here is a detailed documentation of the papers and links we used for this project:

| Reference | Link |
|-|-|
| Feature Extraction for NLP | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8999624&tag=1 |
| NLP based sentiment analysis on Twitter | https://ieeexplore.ieee.org/document/7219856 |
| Deep Learning Model-Based Approach for Twitter Sentiment Classification | https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9373371 |

## Notebooks

We include two Jupyter Notebooks for the code

- The first NoteBook ([BERT_sentiment_analysis_using_Youtube_Comments.ipynb](./BERT_sentiment_analysis_using_Youtube_Comments.ipynb)) is used to test the sentiment analysis on YouTube comments Kaggle data.

- The second NoteBook ([Comparing-TF-and-PT-models-SQuAD.ipynb](./Comparing-TF-and-PT-models-SQuAD.ipynb)) used to test the sentiment analysis on YouTube tweets data.

## Results
1. For Youtube comments 
The first code "BERT_sentiment_analysis_using_Youtube_Comments.ipynb" we got these results.

Our BERT model has giving us 70% accuracy on the test data.

![image](https://user-images.githubusercontent.com/83011466/196296921-76b9cbfa-6e26-47b5-b8f0-f9efe0b4b8aa.png)

2. For Youtube tweets

## Discussion

## Future Work
