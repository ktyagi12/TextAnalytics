**AIM:** Supervised Machine Learning Techniques

Programming Language: Python 3.x
IDE: Jupyter

**Tasks:**

**1. K-NN:**
a. Supervised Machine Learning algorithm,k-NN, applied to the famous Iris Data set.Two parameters are interesting: 
(i) the split which is the size of the training subset v test subset (split = .67) means roughly 2/3rds training, 1/3rd testing.
(ii) k which is the size of nearest neighbors. Note, the Accuracy of model is determined for test sets; it measures how well it classifications work for the unseen set.

b. Taking ideas about cross-validation into account; systematically vary the size of the split; exploring a decent number of other values for it >0.0 and <0.9. Also systematically vary k on five selected values between 1 and 20.

c. Plot the accuracy in a graph for these parameter changes.

**2. Bayes Classifiers**
The nltk Bayes classifier that does the prediction of male/female names based on the last letter in the name.
Think of a new feature that you could extract from the data-set; define a function for it (modifying gender_features) and see what is learned from it in the classification.

**3. SVMs**
Learning hand written digit recognition.
a.Now run three different training configurations and then test the outputs for 5-10 different digits;

**Supervised Machine Learning Technique: kNN Algorithm**

-k-nearest neighbors algorithm(k-NN) is a non-parametric method used for classification and regression algorithm.It is a supervised algorithm in which an object is classified by a majority vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors. It makes the use of distance metric to check the similarity among the neighbors and the test sample.

-Split value determines the split percentage of training and test set. 

-k in k-NN determines the number of data points closer to the test sample. Accuracy tells how well the test point is classified.

![image](https://user-images.githubusercontent.com/38240162/72671798-c88d1680-3a47-11ea-944e-03192ec0d849.png)

-Cross Validation is a model validation techniques for assessing how the results of a model will generalize to an independent data set.
 It define a data set to test the model in the training phase in order to limit problems like overfitting, underfitting and get an insight on how the model will generalize to an independent data set. 

-Split values are considered as follows: 0.2,0.4,0.6,0.8 

-For every split value, k values are as follows: 1,5,10,15,20

-When the value for k gets increased, accuracy gets decreased as the algorithm will look for more data points in the neighborhood and hence increase the (underfitting)generalisability at the cost of variance.

-When the value for the split is eventually increasing(training dataset gets increased), the larger the percentage of training sets, the better the classification because the classification accuracy will be relatively close to the optimum value and then it can obtain an acceptable optimum value.

![image](https://user-images.githubusercontent.com/38240162/72671802-d80c5f80-3a47-11ea-9b99-68227f741c48.png)

![image](https://user-images.githubusercontent.com/38240162/72671806-eeb2b680-3a47-11ea-9dca-77ee0f8c3ec5.png)

-Cross Validation has a single feature known as ‘k’ that indicates the number of partitions that a given data set is to be split into.That’s why it is called k-fold cross-validation.

-Dataset gets divided into K equal folds, here it is given as 5 fold, so the dataset is divided into 5 partitions. For every iteration(till k), consider 1 partition of the dataset as the test set and remaining all portions as training set.

-Then a model is fitted on the training set and tested for the test set.

-Evaluation score is calculated for every iteration collectively using metric like mean.

-The difference between the Hold Out and Cross validation is that here, split value is specified. Instead it automatically divides the dataset but in ‘K’ equal parts.

-The results of a k-fold cross-validation run are often summarized with the mean of the model skill scores.

-Every partition of the dataset becomes test set once and remains in the training set for (K-1) times.(Bias gets reduced and the variance gets increased as the value for ‘K’ increases.)

**Naive Bayes Classifier:** A Naive Bayes classifier is a probabilistic machine learning model used for classification task based on the Bayes theorem.

![image](https://user-images.githubusercontent.com/38240162/72671813-1a35a100-3a48-11ea-990b-6a1fdf68fecc.png)

**Support Vector Machines:** SVM are supervised learning models for classification and regression problems. They are used for both linear and non-linear problem.

-The idea behind SVM is to create hyperplane that separates the classes in the case of classification. The data points lying on the hyperplane or closer to the hyperplane are called the support vectors. They influence the position and orientation of the hyperplane.The goal is to maximize the margin between the points on either sides of the hyperplane. Thus model can easily predict target labels for the unseen data points.

**Digit Recognition:** It is the working of a machine to train itself to recognize the digits for online handwriting recognition as the handwritten digits can vary in size, shape, width, orientation so the issue is wrongly classifying the digits due to the similarity between digits such as 1 and 7, 5 and 6, 3 and 8 etc.

**Hyper parameter C:** The C parameter determines the influence of misclassification, it shows how much misclassification can be avoided in the svm while classifying the training example.

-Larger values of C, smaller-margin hyperplane if that hyperplane does a better job of getting all the training points classified correctly. 

-Smaller values for C cause the svm to look for a larger-margin separating hyperplane, even if that hyperplane misclassifies more points.

**Hyper parameter gamma**: gamma is a parameter used for non linear hyperplanes.

-Larger values of gamma, model tries to exactly fit the training data set.

-Increasing gamma can lead to overfitting as the classifier tries to perfectly fit the training data.

![image](https://user-images.githubusercontent.com/38240162/72671825-5e28a600-3a48-11ea-9b55-364735a8d81e.png)

**Conclusion:**
Supervised Machine Learning Techniques: k-NN, SVM and Naive Bayes algorithms are applied on textual data and evaluated with varying hyper parameters.
