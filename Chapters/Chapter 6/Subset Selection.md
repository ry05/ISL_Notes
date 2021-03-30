# Subset Selection

Idea: Get a subset of p predictors

## Best subset selection

1. First create M_0, the **null model** that has no predictors => predicts the sample mean for each observation
2. For each k in {1,2,...,p}:
	1. Find M_k, where M_k is the **best of all models** considering a fit of the subset of k predictors
	2. Best is decided by lowest R2 measure
3. Choose best model of all M_0, M_1, ..., M_p using CV, AIC, BIC or adjusted R2 => **Best Model**

### Con
- Inefficient due to large computation time when p is large
	- For p predictors, we will need to fit 2^p models
- Such a large search space can lead to overfitting

## Forward stepwise selection

1. Start with M_0, null model with no predictors
2. Fit p models with a single predictor => Choose the best model of these => Call is M_1
	1. Remove f from the set of predictors p
3. Now, fit p-1 models with 2 predictors where one of the predictor is what is already present in M_1
	1. Remove this newly augmented predictor
4. Repeat till all predictors are gone through
5. Choose best of M_0, ..., M_p => **Best Model**

> Key difference from best subset: Looking at every possible model that contains one predictor more than M_(k-1).

> For p predictors, number of models => Around p^2 (much lesser than 2^p). Exact number is 1 + p(p+1)/2

> Can be used for *large p or p < n*

RSS from forward stepwise is going to be above the RSS values in best subset because *it is possible that the best model having k predictors might not necessarily be a the best model having k-1 predictors*. **Check the figure below.**

![[Pasted image 20210324190738.png]]

Such discrepancies occur only when there is *correlation between the predictors*.

## Backward stepwise selection

1. Start with the full model with all predictors => M_p
2. Remove least useful predictor at each step
3. Do this till you reach null model
4. Choose best of M_0, ..., M_p => **Best Model**

> Same number of models for p predictors as forward subset

> Requires that *n > p*

But, how to choose the best/optimal model? => [[Choosing Optimal Model]]
