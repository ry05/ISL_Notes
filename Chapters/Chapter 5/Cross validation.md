# Cross Validation

Idea: To get test error by applying the model

## Why do we need cross validation?

- Test error can be very different from training error
- ![[Pasted image 20210324104626.png]]
- Check [[The Bias-Variance Tradeoff]]
- When test error decreases even though training error decreases, we call this **overfitting**

## Validation set
- Have a **holdout set**, use this as validation data to compute test error
- This split of the training data into train and validation is done randomly
- ![[Pasted image 20210324105446.png]]
- 50:50 split
- Problems
	- If n is small, data loss => underfitting
	- Relies too much on *where the split was made* => very high variance
	- Validation set error will *overestimate test error* => Why? => As train data is less, error will naturally be more

## Approaches to CV

### K-fold CV
- Divide data into K(equally) sized partitions => folds
- Iterate over the entire data K times
	- Each time, one of the K folds is the validation set and the other (K-1) folds are the training sets
	- A validation error is computed for this iteration
- The mean of all K validation errors gives the test error estimate => cross validation error
- ![[Pasted image 20210324110156.png]]
- ![[Pasted image 20210324110249.png]]
- K is usually 5 or 10
- When K=n, we have **Leave One Out CV**
	- Makes prediction on 1 observation while training on (n-1) observations
	- Advantage => Almost as close as *training on the entire data* => Low bias
	- Problem with LOOCV => Estimates of each fold are correlated => Average can have high variance
- Problems with CV
	- Higher bias as K gets larger
	- K=1 has low bias, but high variance

## Using CV wrong

Consider
1. p=5000, n=5
2. Find 100 predictors with top corr with target
3. Apply logistic classifier on 100 predictors

Question: Can we apply CV in step 3 forgetting about step 2? **NO!**

**Why?**  
In step 2, the procedure has already seen models.

**Solution**  
Make folds before doing any preprocessing.

