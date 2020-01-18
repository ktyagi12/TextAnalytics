# SIMILARITY MEASURE AMONG TEXTUAL DATA.

**AIM:**  Calculate the similarity between the documents using various techniques such as Jaccard Distance, Dice Index, Cosine Similarity, etc.

Programming Language: Python 3.x

IDE: Jupyter

**Tasks:**
1. Make up your own set of word features describing 6 different entities; with some obvious overlaps and
differences.

![image](https://user-images.githubusercontent.com/38240162/72671491-3125c480-3a43-11ea-84dd-19bde6227e25.png)

	a. Modify the Jaccard-Index python program to do Jaccard-Distance and then compute all pairwise
	   distances between the entities. Based on results, show empirically, that the property of triangle inequality holds for measure.
	   
	b. Now implement the difference function for the Dice Coefficient and show that the property of triangle
	   inequality may not hold for this measure.
	
2. Calculate the cosine similarity among the documents.
	a. Find 3 short documents about which you might want to know their similarity. Produce 5 variants on one
	   of the documents and see how the cosine similarity changes.
	   
	b. Plot the similarity differences on a graph showing their cosine similarity score. Verify that your intuitions about what makes the differing docs less similar does indeed lead to scores that are less similar.
	
	c. Find a python package that computes cosine similarity and euclidean distance. Use it process the data
	   you have already. Do the answers for Cosine Similarity correspond? What do the Euclidean Distance scores
	   look like relative to the Cosine ones?
	   
3. Create or find 5 “normal” tweets from Twitter. Now take one of these tweets and systematically generate 20 SPAM tweets from it; using the typical techniques of spammers. Now, perform comparisons between these 20 SPAM tweets each of the 5 Normal Tweets. Plot their edit-distance scores in a graph and colour code to show how the SPAM v Normal ones. Are the SPAM tweets obvious, if not why?


**SIMILARITY MEASURES:**

**Jaccard Index:** It is a statistic used to measure the similarity between finite sample sets, and is defined as the size of the intersection divided by the size of the union of the sample sets: J(A,B) = |A & B|/|A|B|.

**Jaccard Distance:** It is a statistic that measures dissimilarity between sample sets, is complementary to the Jaccard coefficient and obtained by subtracting Jaccard Index from unity: d(A,B) = 1- J(A,B).

**Triangle Inequality Property:** It states that for any triangle, the sum of the lengths of any two sides must be greater than or equal to the length of the remaining side, d(a,c) <= d(a,b) + d(b,c).

**Dice Coefficient:** It is a statistic used to measure the similarity of two samples, defined as twice the size of the intersection divided by the size of the union of the sample sets: DSC(A,B) = 2*|A & B|/|A|B|.

**Dice Distance:** It is defined as semi metric version of Jaccard Index(not a proper distance metric) because it does not hold true for the triangle Inequality measure every time, defined as subtracting Jaccard Index
from unity: d(A,B) = 1- DSC(A,B).

**Cosine Similarity:** It is a metric used to measure how similar the documents are irrespective of their size. It is based on count of the maximum number of common words between the documents. The smaller the cosine,
more similar the vectors.

![image](https://user-images.githubusercontent.com/38240162/72671499-4e5a9300-3a43-11ea-8a20-da6ec968ca99.png)

**Levenshtein Distance:** It is a string metric for measuring the difference between two sequences.

**Conclusion:** 
A plot of edit-distance score is shown below.
The graph depicts that the distance between spam tweets and the normal tweets. Spam tweets are obvious
due to similarity between them and normal tweet whose variants they are as distances between them is less
as compared to that of spam tweets and other normal tweets.

![image](https://user-images.githubusercontent.com/38240162/72671503-629e9000-3a43-11ea-96bf-c633d03d527d.png)
