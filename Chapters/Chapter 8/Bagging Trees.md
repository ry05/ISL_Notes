# Bagging or Bootstrap Aggregation

Idea: Average a set of observations to reduce variance

## How is it done?
1. Use bootstrap to take repeated samples from the same training data
	1. Take B different bootstrap training datasets
2. Get the prediction at a point x in each of the B training sets
3. Average all predictions to get the aggregated prediction for regression. For classification, take a majority vote

![[Pasted image 20210327095140.png]]

> Pruning trees reduces variance, but increases bias. Bagging reduces variance and does not increase bias

## Out of Bag Error estimation

1. Each bagged tree has 2/3 of all training data and 1/3 is left out
	1. The 1/3 that is left out is called out-of-bag(OOB)
2. For predicting response of the ith observation, use each of the trees in which the observation was OOB. This will give B/3 predictions for ith observation
3. Average these to obtain the estimate


