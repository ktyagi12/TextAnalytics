# SIMPLE FREQUENCIES

**AIM:** To familiarize with the term frequencies, word cloud, n-grams, normalization of frequencies.

**TASKS:**
1) Load up the various packages you need for using the wordcloud packages in R:

a. Carry out the commands shown in the practical notes:
> library(wordcloud)
> library(tm)
> wordcloud("May our children and our children's children to a thousand generations, continue to enjoy the benefits conferred upon us by a united country,
and have cause yet to rejoice under those glorious institutions bequeathed us by Washington and his compeers.", colors=brewer.pal(6,"Dark2"),random.order=FALSE)

![image](https://user-images.githubusercontent.com/38240162/72670804-fd926c80-3a39-11ea-9a42-50da59ae1eb9.png)

b. List of the words from the original quote that are included in the wordcloud and the list of those that are not.

![image](https://user-images.githubusercontent.com/38240162/72670808-100ca600-3a3a-11ea-87c9-edee12f98fd3.png)

c. Again, using your word-list add more repeated words and see what happens? Can you change the package’s to make it more inclusive of the
words in the word-list?

![image](https://user-images.githubusercontent.com/38240162/72670819-2450a300-3a3a-11ea-89e1-fecf59628ea2.png)


2) Using an Excel spreadsheet set up your own list of 15 words and give each a made-up frequency between 0 and 2000 for each of three years
(2010, 2011, 2012). Now perform two different normalisations on them:

![image](https://user-images.githubusercontent.com/38240162/72670827-3fbbae00-3a3a-11ea-82ef-a53834714a73.png)

a. Method1: produce a normalised frequency for each word in each year, using the total N of words over all the years (i.e., Grand Total)

b. Method2: produce a normalised frequency for each word in each year, using the total n of words in a given year

c. Does normalising by method1 or method2 make a big difference to the scores produced? Graph the difference and comment on it.

![image](https://user-images.githubusercontent.com/38240162/72670832-5530d800-3a3a-11ea-81a2-32a6037ff1c6.png)

**Conclusions:** 
