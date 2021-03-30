# K-nearest Neighbors

Based on nearest neighbor method (discussed in [[Statistical Learning]]).

## Steps
1. Fix the value of k
	1. k=5 indicates a neighborhood of 5 data points around the point we are classifying
2. Find the class that has most data points in this neighborhood
3. Assign the point to classify to the class that "owns" most data points in this neighborhood

> The value of k determines the performance of the model; k is a **tuning parameter**
> k is too small? **Overfit!**
> k is too large? **Underfit!**

![[Pasted image 20210322170120.png]]




