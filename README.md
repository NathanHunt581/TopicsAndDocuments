# Topics and Documents - RoboTop

## Overview

In this project, I applied topic document modeling to a corpus of 15000 news articles.  I imagined a human assigned the same task, and thought that anyone victimized with this might choose to limit the number of topics, creating an "other" pile for  articles not clearly corresponding to one or a few of the topics.  I developed an iterative procedure to do just this by discarding articles assigned to a large number of topics.  The approach gives reasonable results, evaluated either by coherence and perplexity scores or by manual inspection of the resulting topic - document correspondence.

## Data

The corpus used is 15000 articles from 15 US publications.  I am not including the corpus on GitHub.  It is available at

https://www.kaggle.com/lenamkhanh/analyzing-the-news/data

The entire data set is 143000 articles.  I chose to work with a subset of 15000, 1000 from each of the publications. This number seemed adequate for my purposes.

## Methods

I used the gensim library for preprocessing and the SpaCy library for lemmatization and stop word removal.  SpaCy was also used for named entity recognition, and named entities were repeated three times in the bag-of-words to give them increased weight.  

I used gensim's implementation of latent Dirichlet analysis (LDA) for topic - document modeling.

The iterative procedure uses the entropy of each document's loadings over topics.  After a round of LDA, the entropy of each document with respect to the topics is calculated, and those documents having entropy in the top 5% are dropped.  This procedure is repeated until a stopping criterion is satisfied.  Various stopping criteria could work - I ended up requiring that the mean entropy be less than a threshold.

See the notebook for details.


## Conclusions



