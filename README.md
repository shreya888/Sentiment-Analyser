
# Sentiment-Analyser

**AIM :**
The project aims to do sentiment analysis for the purpose of identifying sentiment in movie reviews using the IMDB movie reviews dataset and then applying a simple Bag of Words model to get predictions of whether a review is thumbs-up or thumbs-down.

------------------------------

**INTRODUCTION :**
Sentiment analysis is an interesting topic in machine learning. People express their emotions in language that is often obscured by sarcasm, ambiguity, and plays on words, all of which could be very misleading for both humans and computers.

--------------------------------

**MOTIVATION FOR THE PROJECT :**
  The goal of Sentiment Analysis is to harness  data in order to obtain important information regarding public opinion, that would help make smarter business decisions, political campaigns and better product consumption. Sentiment Analysis focuses on identifying whether a given piece of text is subjective or objective and if it is subjective, then whether it is negative or positive.

--------------------------------

**DESCRIPTION:**
  The necessary file can be downloaded from the  Github repository [Sentiment-Analyser](https://github.com/shreya888/Sentiment-Analyser). The  file that is needed is TrainData.tsv, which contains 25,000 IMDB movie reviews, each with a positive or negative sentiment label.
Next, we read the tab-delimited file into Python. To do this, we can use the *pandas* package which provides the *read_csv* function for easily reading and writing data files.

 - **Data Cleaning and Text Preprocessing**
    First, we'll remove the HTML tags. For this purpose, we'll use the *BeautifulSoup* library.
    
 - **Dealing with Punctuation, Numbers and Stopwords: NLTK and regular expressions**
    To remove punctuation and numbers, we will use a package for dealing with regular expressions, called *re*.
    Finally, we need to decide how to deal with frequently occurring words that don't carry much meaning. Such words are called "stop words"; in English they include words such as "a", "and", "is", and "the". We can use  Python packages that come with stop word lists built in. We import a stop word list from the Python _Natural Language Toolkit(NLTK)_.
    Now we have code to clean one review - but we need to clean all training reviews! To make the code reusable, created a function that can be called many times.(review_to_words)
    
 - **Creating Features from a Bag of Words (Using scikit-learn)**
    Now that we have our training reviews tidied up, we convert them to some kind of numeric representation for machine learning. One common approach is called a Bag of Words. The Bag of Words model learns a vocabulary from all of the documents, then models each document by counting the number of times each word appears.
    We'll be using the _feature_extraction_ module from _scikit-learn_ to create bag-of-words features.
    
 - **Random Forest**
    At this point, we have numeric training features from the Bag of Words and the original sentiment labels for each feature vector, so we do some supervised learning!
    Here, we'll use the _Random Forest classifier_. The Random Forest algorithm is included in scikit-learn (Random Forest uses many tree-based classifiers to make predictions, hence the "forest"). Below, we set the number of trees to 200 as a reasonable default value.
    
----------------------------------------
    
**RESULTS :**
Using the trained Random forest classifier on the test set we achieve an accuracy of 84.81 Percent on test set.
