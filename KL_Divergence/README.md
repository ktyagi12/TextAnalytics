**AIM:** SENTIMENT USE BY K-L DIVERGENCE

Programming Language: Python 3.x

IDE: Jupyter

**Tasks:** 

1.Take the simple sentences and compute the K-L divergence scores for them, in both directions.
Now create a third story that is very different to the other two, add it to the program and report how its score changes relative to the first two.
Explain what role epsilon and gamma play in the computation of K-L.

**KL Divergence:**
The Kullback–Leibler divergence,KL Divergence is a measure of how one probability distribution is different from a second, reference probability distribution.
For 2 documents, d1 and d2 let p and q be the probability distributions of documents 1 and 2.
Two properties:
Summation of p and q equals 1
For each i, p(i) and q(i) should be greater than one.
Then KL Divergence(Doc1||Doc2) is defined as summation of product of document 1 and logarithm of ratio of document1 to document 2.

![image](https://user-images.githubusercontent.com/38240162/72674045-1dda1f80-3a6a-11ea-9b9f-a092fe001d26.png)

where,Q(i) is the approximation and the P(i) is the true probability that is considered in matching Q(i).
It has 3 properties:
	KL Divergence(Doc1 || Doc2) is not same as KL Divergence(Doc2 || Doc1) due to asymmetry.
	If both documents have exactly same common words, KL Divergence is 0.
	It is additive for independent distributions.

The KL divergence infers that how well the probability distribution Q approximates the probability distribution P by calculating the cross-entropy minus the entropy.

**KL Divergence Score:** KL Divergence Score takes the values between 0 and infinity. The lower the value of KL Divergence Score,the better true distributions are matched with the approximations

**Entropy:** The measure of randomness in the information being processed.

**Cross Entropy:** It is a measure from the field of information theory, building upon entropy, calculating the difference between two probability distributions. 
KL Divergence calculates the relative entropy between two probability distributions, whereas cross-entropy can be thought to calculate the total entropy between the distributions.

![image](https://user-images.githubusercontent.com/38240162/72674052-34807680-3a6a-11ea-91dd-03ffa256085a.png)

KL divergence, (relative entropy information gain or information divergence) of q(x) from p(x) measures how much information is lost when q(x) is used to approximate p(x). And it is different from the information lost when p(x) is used to approximate q(x). So the KL Divergence between documents 1 and 2 are different when calculated in both directions.
The documents 1 and 2 have more common words due to which their probability distribution is quite similar and thus the KL Divergence score is low.

**Hyper parameters:** 
While calculating the KL Divergence among the 2 documents, we end up with 2 major problems:
1.KL Divergence is calculated in both directions due to the asymmetry.
2.Only the common terms among both documents are considered.
So, to avoid such drawbacks, Instead of using the common terms, whole vocabulary is to be considered.Thus smoothing comes but with Smoothing, the probability distribution doesn’t sum up to 1. So, back off smoothing that keeps the probability distribution sum to 1 and whole vocabulary is considered instead of common ones.

To avoid such values of KL Divergence, hyper parameters are used:

**Epsilon:** It is defined as the probability of a term which is not in a document. It is set to a small value instead of 0 to avoid the distance to be infinite. It is a value less than the minimum term probability occurring in either of the documents. Every word in the document is assigned a threshold probability instead of only to the common words.
	
**Gamma:** It is defined as a normalization coefficient to account of epsilon, so a probability of a term in a category satisfies the properties of a probability (sum to 1).

**Conclusion:** KL- Divergence between documents is calculated and shown above with examples.
