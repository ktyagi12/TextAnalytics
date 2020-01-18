**AIM:** Unsupervised Machine Learning Techniques

**Programming Language:** Python 3.x

**IDE:** Jupyter

**Tasks:** 

1. Have a look at the simple k-means program you have been given. Note,it can look for clusters of different ks; but for plotting purposes it fixed to look for k=3. The program can work from a randomly generated set of points or a defined set.

  a. Use the init_board fn to randomly generate 15 points; store this output and set the data variable to it.
     Now run this set 10 times and note the clusters found by k-means. Report the results of these runs and the extent to which the same clusters are found.

2. Now, create you own set of data, again with 15 points. You should construct this data-set to have very clear clusters (a bit like the simple 6-point example shown). Now run this set 20 times and note the clusters found by k-means.

3. Do some research on the problem that k-means produces different answers on different runs. Describe two typical solutions to this problem with references to the literature you read to answer his question.

**Clustering:** It is the unsupervised face of machine learning given the data as unlabelled. It labels the data points based on how they are groped together.
 
**K-Means Clustering Algorithm:**
-K- Means clustering is a unsupervised learning algorithm. It is used when the data is not defined in groups or categories i.e. unlabeled data.

-This algorithm is an iterative algorithm that partitions the dataset according to their features into K number of predefined non- overlapping distinct groups. It keeps the data points within the clusters as close as possible and also tries to keep the clusters as far as possible. (Less Intra-cluster distance and More Inter-Cluster distance).

-It clusters ‘n’ data points into ‘k’ clusters where each data points is a part of that cluster with least mean. It runs on Euclidean distance metric calculation in order to find the cluster for the data points.

![image](https://user-images.githubusercontent.com/38240162/72672036-f1170f80-3a4b-11ea-9ad7-cc3138b3519a.png)

KMeans clustering algorithm produces different answers on different runs because:

-KMeans is a probabilistic technique. It uses random starting values for the centroid.That's why in such a optimization/machine learning problems, multiple iterations are run for the KMeans algorithm and a validation data set can be sued if possible.

-KMeans clustering algorithm places the initial seeds (cluster centers) randomly. So each run of the algorithm will have a different initial set of seed locations, and as such (slightly) different outcomes. The algorithm is often executed multiple times and there is an error measurement calculated as the mean square distance of each point to the cluster centroid to which it belongs.

-Starting with predefined initial seeds instead of randomly selected seeds for the centroids will ensure a consistent answer.

-There is a certain random part in the algorithm that repeatedly uses the random starting points to find the global solution. But due to the pseudo-random nature of the algorithm,slightly different clusters are obtained each time.

-KMeans may not find the global optimum value (random initial points).

-KMeans may not find the global optimum value for number of data points in a cluster.

-As the location of the initial centroids is random, results may not be comparable and show lack of consistency. Also, K-means produces clusters with almost equal number of data points in it, although the data might be different completely and it’s very sensitive to outliers and noisy data.

**Two typical solutions to this problems:**

**I.KMeans++ Algorithm and Single Pass Seed Selection (SPSS):**

-This helps in robust seed selection to improve the clustering results.

-Single Pass Seed Selection, which generates single and optimal solution for the initial seeds and this technique is insensitive to the outliers.

-This algorithm selects the start seeds with particular probabilities.

-This algorithm selects the high density point as the first centroid and also it calculates the minimum distance that separates the centroid.

-The major tasks for Single Pass Seed Selection is to: 
-Select optimal centroids
-Generate single clustering solution instead of different results on different runs.

-It is a method of initialization to the KMeans algorithm. It first initializes the seed and based on high density, distance is calculated to separate the centroid.

Step 1: Initialize the first centroid with a point which is close to more number of other points in the data set. 

Step 2: Calculate the distance matrix(Distance between all data points)

Step 3: Assume that m (total number of points) points are distributed uniformly to k clusters then each cluster is expected to contain m/k points. Compute the sum of the distances from the selected point (in Step1) to 		  first m/k nearest points and assume it as y.

Step 4: Find the index of minimum value of Sum from Step3 and find highest density point X.

Step 5: Add the high density point to the Centroid set as the first centroid.

Step 6: For each point Xi, calculate distance (Xi) to be the distance between Xi and the nearest point in Centroid set.

Step 7: Calculate the sum of distances of first m/k nearest points from the X as y.

Step 8: Find the unique integer i so that Sum of all squared distances(Xi) >= y > Sum of all distances(Xi i from 1 to i-1).

Step 9: Add Xi to Centroid set.

Step 10: Repeat steps 5-8 until k centroids are found 

-k-means++ algorithm is to careful select the initial seeding for k-means algorithm. However, It has to run multiple number of times for good clustering results but still produces different results in different independent runs. 

-The Single Pass Seed Selection yields unique solutions with consistent clustering results using the high density point as the first seed. Thus it is insensitive to the outliers and avoids re runs for the algorithm.

**II.Furthest Point Heuristics (Maxmin):**

-Initialization done through Maxmin reduces the error rate of clustering on an average from 15% to 6%..

-Repeating it n times reduces the error rate to 1%.

-It selects an arbitrary point as first centroid and then adds points one by one to the centroid set by calculating the maximum distance from the minimum (nearest) already existing centroids.

-For every data object, counter is maintained to its nearest neighbor. When another centroid is chosen, distance from all the data points to the new centroid is calculated and if the distance is less than that of previous, counter is updated. This results in N distance calculations and hence it gets repeated k times, resulting in kN time complexity.

-Further when the new centroid is to be selected, it is done by furthest point from the subset of the data rather than complete dataset. 

**Algorithm works as follows:**

Step1: Choose centroid at random initially.

Step2: Then for every data points, choose next centroid which is farthest from the previously selected centroid. It fixes the Gaussian problem but it is sensitive to outliers.

-Only the initial point is selected randomly, the rest of the points are selected deterministically. Then for each point in Xi = [Xi,1,Xi,2……..,Xi,m]. Every point is described by m features. A function f(xi,j) is used to calculate the frequency count for every attribute value.

  -Then a scoring function is defined (Summation of all function f(xi,j)) to evaluate the data point and point with highest score will be chosen as first point and remaining are selected the same way.
  
  -The points that contain attribute values with higher frequencies most probably becomes the centers.All the rest of the points are selected deterministically. This shows that fixed clustering results could be achieved from our new initialization procedure based k-modes clustering algorithm.

  -The time complexity to choose first point is : O(n) with two scans over the dataset:
	
  1. m number of hash tables are constructed to store attribute values and their frequencies.
	
  2. Frequency count of an attribute value from the corresponding hash table is fetched in O(1).

-Hence the time complexity for data point with largest score is O(n).

-Thus, the overall time complexity of new farthest-point heuristic is still O(nk).

**Conclusion:** Unsupervised Machine learning technique K-Means CLustering technique applied on various data points are shown above with examples..

