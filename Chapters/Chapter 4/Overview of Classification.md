# Overview of Classification

Response feature has discrete values.

Example:
eye_color could be {blue, black, brown}
email could be {spam, ham}

A classification function

$$C(X) \in Classlabels$$

where Classlabels is the set of all plausible labels that can be assigned to an observation in the dataset.

> Classification is often treated as a task of estimating the *probabilities* of a particular data point belonging to a each category in Classlabels

## Why can't we use linear regression?

An idea is to use linear regression and use a threshold to make a classification.

- This works well for a binary classification problem (based on simple probability theory)
	- Not good when num of classes > 2 as it assigns ordering to the class labels
- But, linear reg could create probabilities < 0 !

Hence, we need a function that won't go less than 0 => Enter [[Logistic Regression]]

## Evaluating classifiers

[[Confusion Matrix]]