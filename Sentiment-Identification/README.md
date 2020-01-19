**AIM:** Sentiment Identification : Inter Rater Reliability using Kappa and Pearson's rho.

Programming Language: Python 3.x

IDE: Jupyter

**Tasks:** 

1. Human Ratings Task:
a) Get 3 classmates (opinion holders) to write three different opinions about their phone.
b) Get 3 different people (raters) to rate these comments as positive, negative, neutral.
c) Take this 3 x 3 matrix and find the inter-rater reliability between your 3 raters using Kappa.
d) If you wanted to get the correlation between raters (using Pearson’s rho) what would you do? Then do this.

2. Do, some searches and find 3 sentiment lists that are commonly used in previous research. For 2 of these lists,
select 10 positive and 10 negative words (randomly). Evaluate each word, discussing whether it is really
positive/negative; for each one try to find a sentential context in which it might be interpreted with the opposite
valence.

3. Bromberg’s Sentiment Program:
Have a look at the simple program that does sentiment analysis. So, take a look at the program and see what is
happening in the different variables, but adding print statements on its variables.
a) Now consider ways to improve the training. Eg if you removed stopwords from the inputs what do you think might
happen?
b) Implement this or another solution in the program and report what happens to the precision and recall of the
classifier.

**Opinions:** Opinion is defined as a judgement which is not conclusive. Opinion holder is one who expresses their opinions
on a subject.
3 opinion holders with 3 different opinions about their phone are considered.
Opinions are as follows:

![image](https://user-images.githubusercontent.com/38240162/72673652-9b4f6100-3a65-11ea-8bc0-76becd4b7c17.png)


**Rater:** One who determines a rating for a particular subject is called a Rater.
Possible rating values can be (Positive, Negative , Neutral).

**Inter-rater Reliability:** It is defined as the extent of agreement among the raters. It is the score of how much consensus
exists between the ratings given by different raters. High value of Inter- reliability infers to high degree of agreement among the raters. It can be evaluated by different statistics such as Kappa, Pearson, Percentage agreement etc.

**Cohen’s Kappa Coefficient (k):** It is a statistic used to calculate the inter-rater reliability for categorical values.
The coefficient k considers the agreement occurring by choice. K value always less than or equal to 1. A value 1 depicts
perfect agreement.

![image](https://user-images.githubusercontent.com/38240162/72673684-f97c4400-3a65-11ea-8d6c-d150b49a7f12.png)

where
po: Relative agreement among raters.
pe: Probability of chance agreement


**Pearson’s rho:** It is defined as the measure of linear correlation among 2 variables. It’s value lies in between -1 and +1.
+1 infers total positive linear correlation among raters in this case.
-1 infers total negative linear correlation among raters in this case.
0 infers zero linear correlation among raters in this case.
It can be calculated as:

![image](https://user-images.githubusercontent.com/38240162/72673730-760f2280-3a66-11ea-8879-c56b248e10c9.png)
where,
cov(X,Y): Co variance between X and Y.
σX : Standard Deviation of X
σY : Standard Deviation of Y

**Conclusion:** Inter Rater Reliability using Kappa and Pearson's rho is calculated and shown above with their applications.
