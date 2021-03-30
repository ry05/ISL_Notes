# Clustering

Idea: Find subgroups in data by maximizing inter-cluster distance and minimizing intra-cluster distance

## 2 types

- K-means clustering => You know how many clusters you need
- Hierarchical clustering => You don't know how many clusters you need (can be any from 1 to n), visualized using a **dendrogram**


## K-means

![[Pasted image 20210327183448.png]]

![[Pasted image 20210327183522.png]]

![[Pasted image 20210327183548.png]]

> Depends on the start or random assignment

## Hierarchical clustering

Bottom up or agglomerative clustering

![[Pasted image 20210327183829.png]]

> The number of clusters is dependent on where you cut the tree. See below.

![[Pasted image 20210327183942.png]]

### Types of linkages

![[Pasted image 20210327184334.png]]

Single linkage : Could create asymmetric trees

Centroid linkage: Leads to inversions

> Scaling of features is important in clustering too!

