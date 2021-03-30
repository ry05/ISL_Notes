# Important Questions on Regression

1. Is at least one of the predictors useful in predicting the outcome?
	1. Use the F-statistic
2. Are all predictors useful or only a subset?
	1. Most direct approach: **All subsets or best subsets regression** or compute for all possible subsets and choose
		1. Works only if p is small
	2. Automated approaches:
		1. Forward selection
		2. Backward selection
3. How well does the model fit the data?
4. Given a set of predictor values, what are our our predictions and how good is it?
5. What if there are qualitative variables?

**F-statistic**

![[Pasted image 20210323094710.png]]

## Automated variable selection methods

### Forward selection

1. Start with **null model** - Has only an intercept
2. Fit *p simple linear regressions i.e with one variable in each model* and add to the null model the variable that results in the lowest RSS
3. Next, add to that model the variable that results in lowest RSS amongst all two-variable models from remaining (p-1) models
	1. Think as "which variable must be added to the already selected variable for a low RSS"
4. Continue till a stopping rule is reached

### Backward selection

1. Start with all variables in model
2. Remove the variable with the largest p-value at each step
3. Repeat 2 with (p-1) variables
4. Continue till a stopping rule is reached

## Qualitative predictors

Use **dummy variables**

![[Pasted image 20210323095955.png]]

For a qualitative predictor with more than one level, create more dummy variables!

![[Pasted image 20210323100242.png]]

If both are 0, this person is African.

> For a qualitative variable with k levels, create (k-1) dummy variables
> The level with no dummy variable is known as the **baseline**





