# Principal Component Analysis

Used for data viz or pre-processing before supervised methods are applied.

Idea: Transform high dimensional data into lower dimensions => Find a sequence of linear combinations of variables that have maximum variance and are mutually correlated

![[Pasted image 20210327181948.png]]

> For p features, there can be p principal components

> Principal components are uncorrelated with each other

> There will be atmost min(n-1, p) principal components (to also take care of the case where p > n)

> Standardization is required for PCA

![[Pasted image 20210327182902.png]]

![[Pasted image 20210327183030.png]]

## CV can't work in PCA

Because there is no response here.

When can we use CV? => When you use PCA on regression tasks with a lot of features

