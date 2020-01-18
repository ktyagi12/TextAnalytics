# TERM FREQUENCIES/ INVERSE DOCUMENT FREQUENCIES

**Programming Language Used:** Python 3.x

**IDE:** Jupyter

**WordCloud Generation Tool:** R 

**AIM:** Familiarize with the concepts of term frequency and inverse term frequency.

**Tasks:**
1. Find 10 short text-items (20-30 words); they could be emails, short docs,tweets or whatever… Make
sure they all deal with some common topic of interest; so they have some of the same words.
  a. Remove the standard stopwords from them using some standard list, use nltk.
  b. Compute the TF scores for all the remaining words in the texts and use R to show the word-cloud for
these words.
  c. Now, compute the TF-IDF scores for all the same words in the texts. Construct a set of words that
represents the TF-IDF scores you have found, for all the words. Use R to show a word-cloud for these words.

2. Using Python or R, compute the PMI scores for all adjacent pairs of words in your 10-doc corpus.

3.Entropy has been used to determine whether tweet set is interesting (contains variety) or repetitive
(spam). Create two sets of 10 made-up tweets:
  a. spam-set: where the 10 tweets are very similar containing an advert for a product.
  b. random-set: where the 10 tweets are very different, chosen at random from Twitter.

Now, find a Python/R program or package that computes entropy and find the entropy values for:
(i)spam-set, 
(ii) random-set, 
(iii) the two sets combined.

**Term Frequency, TF:** Frequency of the word in a text document, tf(t,d) = frequency(term t in document d).

![image](https://user-images.githubusercontent.com/38240162/72670210-f87def00-3a32-11ea-83be-c3b96088d244.png)


**Inverse Document Frequency, IDF:** Weight indicating how widely a term is used. (More frequent term -> Less IDF weight).
It is the count of documents in corpus containing term t.

![image](https://user-images.githubusercontent.com/38240162/72670223-1a777180-3a33-11ea-9978-715e5ef0e7c2.png)


**Word Cloud:** Wordcloud depicts the visual representation of the words of all the remaining words. Here it displays that few
terms like kerala, kochi, web,design are most frequent among the documents.

![image](https://user-images.githubusercontent.com/38240162/72670207-e7cd7900-3a32-11ea-9125-8967f4afb4fe.png)

**PMI Score:** PMI is defined as the measure of association. It measures how much more likely the words co-occur than if they were independent in the text. It is calculated as: PMI(word1, word2) = Probability(word1, word2)/ Prob(word1) P(Word2).
PMI is calculated by nltk.collocations.BigramAssocMeasures() module

**Entropy:** Entropy is defined as the sum of the probability of each label times the log probability of that same
label, written as H(A) = -sum(p * log(p), axis=0). It is a measure of randomness of all the words.

**Conclusion:**
Term Frequencies / Inverse Document Frequency Implementation with their applications of examples are implemented in Python with word clouds generated using R.

