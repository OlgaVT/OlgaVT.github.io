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
| <img src="https://github.com/OlgaVT/OlgaVT.github.io/blob/master/images/BBSB-8_2=38.jpg" width="25000">  |K-means clustering is the most popular clustering technique. It partitions data objects into k clusters where k is fixed *a priori*. <ul>K-means clustering steps: <li>Step 0: Decide how many clusters you should have (k)</li><li>Step 1: The algorithms randomly assigns each of the observations to only one of the k clusters</li><li>Step 2a: Next, the algorithm computes the **centroid** of each cluster. The centroid is the mean of feature values for all points in this cluster.</li><li>Step 2b: The algorithm reassigns the observations to their nearest centroid. </li><li>Step 2a: The algorithms starts the next iteration and computes the centroids of new clusters. Then reassigns points to the nearest centroid, recalculates the centroid, and so on. </li><li>The algorithm stops when the centroid finds the local optimum</li></ul><ul>Advantages: <li>Simple and fast</li></ul><ul>Limitations:<li>Need to choose k “manually”</li><li>“Non-deterministic”: depends on initial distribution of points</li><li>Sensitive to outliers and noise</li></ul>|[scikit-learn Python package about clustering](https://scikit-learn.org/stable/modules/clustering.html)|
