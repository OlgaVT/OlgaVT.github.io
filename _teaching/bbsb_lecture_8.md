---
title: "Basics on Bioinformatics and Systems Biology: Lecture 8"
collection: teaching
type: "Lecture"
permalink: /teaching/bbsb_lecture_8
venue: "VU"
date: 2026-01-10
location: "Amsterdam, the Netherlands"
---

Here you will find the basic concepts for the Lecture 8 and link to the additional/support material

## Unsupervised machine learning

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_24.jpg" width="25000">  |**Unsupervised machine learning** operates with unlabeled data and is used to find patterns in such a data. The main approach is **clustering** - grouping together simlar data objects. <ul>Definitions:<li>**Clusters** are groups of data onjects that are more similar to each other than to objects from other groups</li><li>**Clustering goal** is the following: given a set of unlabeled data objects, group them into clusters such that the intra-cluster differences are minimized and the inter-cluster differences are maximized.</li><li>Clustering a dataset can reveal hidden relationships between the observations and features.</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_28.jpg" width="25000">  |The choice of a clustering algorithm depends on a data sctructure to be clustered|[scikit-learn Python package about clustering](https://scikit-learn.org/stable/modules/clustering.html)|

## k-means clustering

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_2=38.jpg" width="25000">  |K-means clustering is the most popular clustering technique. It partitions data objects into k clusters where k is fixed *a priori*. <ul>K-means clustering steps: <li>Step 0: Decide how many clusters you should have (k)</li><li>Step 1: The algorithms randomly assigns each of the observations to only one of the k clusters</li><li>Step 2a: Next, the algorithm computes the **centroid** of each cluster. The centroid is the mean of feature values for all points in this cluster.</li><li>Step 2b: The algorithm reassigns the observations to their nearest centroid. </li><li>Step 2a: The algorithms starts the next iteration and computes the centroids of new clusters. Then reassigns points to the nearest centroid, recalculates the centroid, and so on. </li><li>The algorithm stops when the centroid finds the local optimum</li></ul><ul>Advantages: <li>Simple and fast</li></ul><ul>Limitations:<li>Need to choose k “manually”</li><li>“Non-deterministic”: depends on initial distribution of points</li><li>Sensitive to outliers and noise</li></ul>||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_39.jpg" width="25000">  |<ul>Elbow method (How to choose k):<li>Run k-means clustering methods for multiple k values</li><li>For each k calculate within-cluster sum of squares: a sum of distances between the observations and centroids</li><li>Plot within-cluster sum of squares for different values of k</li><li>Find a point ("an elbow point"), after with there is only a marginal decrease in the sum of squares</li></ul>||

## Hierarchical clustering

| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_41.jpg" width="25000">  |**Hierarchical clustering** is one of the most popular techniques to cluster biological data. <ul>Agglomerative clustering:<li>Treats each data object as a cluster</li><li>Calculate the distance between objects and joins the two closest</li><li>Update the distance matrix</li><li>Continues merging till a single cluster remains</li></ul><ul>Divisive clustering:<li>Treats all data objects as a cluster</li><li>Divide into two clustrs</li><li>Continues till each data object is a single cluster remains</li></ul><ul>Advantages: <li>Intuitive</li><li>No need to specify the number of clusters *a priori*</li></ul><ul>Limitations:<li>Less scalable for bigger datasets</li><li>Sensitive to outliers and noise</li><li>Still challenging to detect the number of clusters</li></ul>||

## Biclustering
| Slide | Text | Additional material|
|----------------|-------------|-------------|
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_50.jpg" width="25000">  |<ul>Clustering limitations:<li>Produces a single partition of samples</li><li>The results are driven by the largest patterns </li></ul>**Biclustering** clusters simultaniously rows and columns (e.g., genes and samples). The resulting clusters are called **biclusters**||
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_57.jpg" width="25000">  |<ul>Buclustering approach example (UnPaSt tool for gene expression):<li>The expression level of each gene across all samples are fitted to a distribution</li><li>The genes with bimodal distribution are kept and binarized </li><li>Genes with a similar binarization pattern are clustered together first</li><li>Within these gene-based clusters, similar samples are clustered together to form a bicluster</li></ul>|[scikit-learn about biclustering](https://scikit-learn.org/stable/modules/biclustering.html) [UnPaSt tool](https://arxiv.org/abs/2408.00200)|
