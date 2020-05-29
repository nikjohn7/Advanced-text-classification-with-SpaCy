# Advanced text classification with SpaCy

In this project, I worked on implementing a fully functioning text classifier using SpaCy.

You can access the Google Colab notebook [here](https://colab.research.google.com/drive/19-uePBR7H_YTa9hA5_I69OWgMMiyY5iS)

## Dataset

Here I have used a dataset of Amazon fine food reviews.

This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories.

[Reviews.csv](https://www.kaggle.com/snap/amazon-fine-food-reviews): 568,454 food reviews Amazon users left up to October 2012

Data includes:

+ Reviews from Oct 1999 - Oct 2012

+ 568,454 reviews

+ 256,059 users

+ 74,258 products

+ 260 users with > 50 reviews


## Sense2vec
Sense2vec word embeddings model works better than word2vec , since it utilises contextual information from words.

The idea behind sense2vec is super simple. If the problem is that duck as in waterfowl and duck as in crouch are different concepts, the straight-forward solution is to just have two entries, duckN and duckV. Trask et al (2015) published a nice set of experiments showing that the idea worked well.

It assigns parts of speech tags like verb, noun , adjective to words, which will in turn be used to make sense of context.

1. Please book [VERB] my ticket.
2. Read the book [NOUN].

.


Here I have made use of Reddit vectors dataset for training sense2vec model. This is a corpus of Reddit vectors from Reddit comments. (trained on all comments of 2015).

Access the folder [here](https://www.kaggle.com/poonaml/reddit-vectors-for-sense2vec-spacy)


## Technology stack and concepts
+ SpaCy
+ sklearn
+ nltk
+ pandas
+ tokenization
+ part-of-speech tagging
+ dependency parsing
+ lemmatization
+ named entities recognition

### Visualizing Data

- explacy - explaining how parsing is done
- displaCy - visualizing named entities


### Word vectors and similarity

sense2vec - using contextual information for building word embeddings

## License
[MIT](https://choosealicense.com/licenses/mit/)
