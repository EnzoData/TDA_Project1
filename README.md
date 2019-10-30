# Topological Data Analysis Project 1

## Introduction
It is apparent that within the field of Data Science, Topology is starting to be heavily used for data analysis. Our main focus for this project is classification. Our objective is to build a successful training model to predict letters from the Latin alphabet through the process of persistent homology. Before delving into our process for achiving our objective, let's first identify and define some key concepts that will be used. 

Firstly starting with persistent homology, this method is used for computing topological features of space in multiple spatial resolutions. With the help of persistent homology, we can detect more persistent features over a wide range of spatial scale and they likely to represent true features of underlying space rather than artifacts of sampling, noise, or the particular choice of parameters.

Another key concept used throughout the project is bottleneck distance, this distance is the cost of optimal matching between points of the two diagrams. We can even include all the diagonal points in the persistence diagram when calculating the optimal distance. This function returns the maximum distance among all bottleneck distances using each element in dimension.

For clustering the group of points in clusters based on their similarity we used agglomerative clustering. It’s also known as AGNES (Agglomerative Nesting). This algorithm work by treating each object as a singleton cluster. Next, pairs of clusters are successively merged until all clusters have been merged into one big cluster containing all objects.

Lastly, for regression, we used multinomial logistic regression.  This classification method generalizes logistic regression to multiclass problems, i.e. with more than two possible discrete outcomes. It is used to predict the probabilities of the different possible outcomes of a categorically distributed dependent variable, given a set of independent variables (which may be real-valued, binary-valued, categorical-valued, etc.).


Now, the following is a brief summary of what will be done to hopefully achieve the objective of classification and prediction. A dataset will be created by reading 10x10 pixel images for each letter in the latin alphabet, which can be found in [Latin Alphabet](https://github.com/EnzoData/TDA_Project1/tree/master/Latin%20Alphabet/Latin%20alphabet.pdf), where the pixel values are 0 if there is no part of the letter and 1 otherwise.  Using the notebook Lower Star Image Filtrations from ripser.py, [Lower Star Image filtrations](https://ripser.scikit-tda.org/Lower%20Star%20Image%20Filtrations.html), combined with different scanning methods, the 0-Dimensional class in each letter will be obtained in order to classify them through their Euclidean coordinates. Once we have obtained the persistent homology for each letter, we will find the pairwise bottleneck distance between letters. From here, an agglomorative clustering method can be applied to the pairwise distances to grab values for the classification test. This will be done for each scanning method used. Then, we will create a design matrix with the values obtained from the agglomorative clusering method and run a simple normal mulitnomial regression. Once we have obtained 100% classification on each letter, testing can be done by changing certain pixel values from 0 to 1 or vice versa and running through our process again to see if the letters are still classified correctly. 

## Types of Scans
In the folder links below, there are examples of scanning methods that can be preformed on the latin alphabet. The scanning methods that were used in order to achieve classifications through our code are as follows: left to right, right to left, probing from left corner, and diagonal scan.
#### [Scanning (pdf)](https://github.com/EnzoData/TDA_Project1/tree/master/Scanning%20Methods)
#### [Scanning (ipynb)](https://github.com/EnzoData/TDA_Project1/tree/master/Scanning%20Examples)

## Algorithm
In the following folder links, the code used to obtain the persistent homology for each letter and the code to achieve classification can be found. 
#### [Looping](https://github.com/EnzoData/TDA_Project1/tree/master/Looping)
#### [Algorithm](https://github.com/EnzoData/TDA_Project1/tree/master/Algorithm)


## Experiments
In the folder link below, the experiments code can be found

#### [Experiment](https://github.com/EnzoData/TDA_Project1/tree/master/Experiment)


## Discussion/Criticism
From the algorithm produced and the results obtained through experiments, we can see that classification was sucessful on the original 26 letters. Our objective of classification was achieved by using left to right scan, right to left scan, probing from left corner scan, diagonal scan, and 5 density scans. The decision to only include 4 scans was due to.....We see that when we introduce noise, our classifier isn't the best. The classifier would improve if we included the regular persistent homology diagram up to dimension 1, and an L_1 regularization term to our multinomial regression. 

## Literature Review
-Pratik and sri Nikhil please complete-


# Authors

* **Enzo Rodriguez** - [EnzoData](https://github.com/EnzoData)
* **Kevin Urure Cruz** - [kevinururecruz](https://github.com/kevinururecruz)
* **Sakshi Solanki** - [sakshisolanki](https://github.com/sakshisolanki)
* **Sri Nikhil Surapaneni** - [srinikhil96](https://github.com/srinikhil96)
* **Shane Putney** - [ShanePutney](https://github.com/ShanePutney)
* **Pratik** - [ppratik1995](https://github.com/ppratik1995)
