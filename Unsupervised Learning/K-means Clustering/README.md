# K-Means Clustering:
The is an unsupervised algorithm. Let's understand it's name first, why K-means? The K represents the number of clusters or groups in simple words in which you are going to divide your data.
The second term, means clustering is used for describing the process, i.e. here we are using the mean of the data or centroid of the groups to create the group. 

The first step is to assign random k number of centroids for each group and then comapre the data point's distance with each centroid and assign in to the group where the distance is minimum. Here the result for each iterations is not exact, because everytime you start the execution, new random points will be assigned and your algorithm will build up from there, that's the only disadvantage. 

Note that, this is unsupervised because we are not telling the solution or any labeled data to find the best cluster but let it figure out on it's own. Let's implement it in Python.

## Python code for K-means clustering:
```python
 import pandas as pd
 # harry potter example for kmeans
```
