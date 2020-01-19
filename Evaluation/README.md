**AIM:** Evaluation of classifiers using ROC, DET Curves and other parameters.

Programming Language: Python 3.x 

IDE: Jupyter

**Tasks:** 
1) Taking this data, can you compute the Precision and Recall for the system at each threshold and identify the threshold values at which it does best,
according to the F1 measure?

![image](https://user-images.githubusercontent.com/38240162/72672985-68a06b00-3a5b-11ea-8dfb-75248f265724.png)

2) Now, can you plot the ROC for this data?

3) Now, can you plot the DET curve for the same data?


**Confusion Matrix:** It is defined as a table used to describe the performance of the model. It allows visualization of the algorithm’s performance. It consists both Predicted as well as Actual classes. 

![image](https://user-images.githubusercontent.com/38240162/72673351-2843eb80-3a61-11ea-9025-aa52b232302f.png)

**True Positive (TP):** A true positive is an outcome where the model correctly predicts the positive class. Observation is positive, and is predicted to be positive also.

**False Positive (FP):** A false positive is an outcome where the model incorrectly predicts the positive class. Observation is negative, but is predicted positive. 

**True Negative (TN):** A true negative is an outcome where the model correctly predicts the negative class. Observation is negative, and is predicted to be negative.

**False Negative (FN):** A false negative is an outcome where the model incorrectly predicts the negative class. Observation is positive, but is predicted negative. 

**Precision:** It defines what proportion of all the predictions that we made with the model are actually true. It is calculated as the ratio of correct positive predictions to the total predicted positive.

**Recall/True Positive Rate:** It is a measure that gives the fraction of all relevant documents that are successfully retrieved. It is calculated as the ratio of correct positive predictions to the total positive examples.

![image](https://user-images.githubusercontent.com/38240162/72673042-67237280-3a5c-11ea-8302-6c466d87ecc9.png)

**F1 Measure:** It is a way of collaborating both Precision and Recall measures of any model with the help of Harmonic Mean of both of them. For uneven class distribution, where accuracy is not an apt measure, F1 measure works there. Higher the value of F1 measure, higher accuracy for the system (mostly).

**False Positive Rate:** The false positive rate is an accuracy metric, calculated as the ratio between the number of negative events wrongly categorized as positive (false positives) and the total number of actual negative events regardless of classification. The false positive rate infers to the expectancy of the false positive ratio.

**ROC Curve:** A receiver operating characteristic curve, ROC curve, is a technique widely used in machine learning to evaluate the classifier’s performance. It condenses the classifier’s performance graphically and allow us to compare the performances of various classifiers.
It is a graphical plot that depicts the ability of a binary classifier system as its similarity threshold is varied. It plots the True Positive Rate against the False Positive Rate for every threshold value between 0 and 1. 

**Area under ROC Curve:** To compare the classifiers, Area under Curve (AUC) is useful to summarize the performance of the classifiers in a single measure. Higher the area under curve, model is better at predicting 0s as 0 and 1s as 1.
Each point on the ROC curve shows a sensitivity/specificity (TPR,FPR) pair corresponding to a similarity threshold. AUC is a metric of how well a parameter can differentiate between two classes (election/non-election).
ROC Curve is shown below with equal scaling on both X and Y axis and pair of (TPR,FPR) are displayed on the graph : 

![image](https://user-images.githubusercontent.com/38240162/72673022-f8deb000-3a5b-11ea-8a2f-06dccda2d213.png)

**False Negative Rate/Miss Detection Rate:** The false negative rate is the proportion of the individuals with positive condition for which the test result is predicted negative. This rate is also known as miss rate.
The false negative rate is an accuracy metric, calculated as the ratio between the number of positive events wrongly categorized as negative (false negatives) and the total number of actual positive events regardless of classification. 

**DET Curve:** Detection Error Trade Off, DET curve focuses on error more and zoom in to the key parts of ROC curve using log axes. 
DET curve, is a technique widely used in machine learning to evaluate the classifier’s performance in terms of error. It plots the Miss Detection Rate against the False Positive Rate with log axes.
DET curve is an evaluation metric in binary classification problem with two classes focus is on how it is incorrectly classifying both classes. It is a graphical plot of error rates for the binary classifier. 

DET Curve is shown below for the Election-Non-Election tweets classifier with log scaling with False Negative Rate on Y -axis and False Positive rate on the X axis.

![image](https://user-images.githubusercontent.com/38240162/72673030-288db800-3a5c-11ea-9a58-6dc07e65a930.png)


 **Conclusion:**
Graphs evaluates the classifier’s performance. Also, Precision, Recall, F1 measure along with other parameters like True Positive, False Positive, Falsee Negative, True Negative are calculated with the given sample input is shown above.
