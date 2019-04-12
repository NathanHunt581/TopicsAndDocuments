# Topics and Documents - RoboTop

## Overview

In this project, I applied topic document modeling to a corpus of 15000 news articles.  I imagined a human assigned the same task, and thought that anyone victimized with this might choose to limit the number of topics, putting articles not corresponding to a topic in an "other" pile.  I developed an iterative procedure to do just this by discarding articles assigned to a large number of topics.  The approach gives reasonable results, evaluated either by coherence and perplexity scores or by manual inspection of the resulting topic - document correspondence.

## Data

The corpus used is 15000 articles from 15 US publications.  I am not including the corpus on GitHub.  It is available at

https://www.kaggle.com/lenamkhanh/analyzing-the-news/data

The entire data set is 143000 articles.  I chose to work with a subset of 15000, 1000 from each of the publications. This number seemed adequate for my purposes.


## Conclusions



