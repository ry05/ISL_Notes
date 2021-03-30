# Shrinkage

Idea: Shrink coefficients towards 0

Can be applied to very large datasets.

## Ridge Regression

Idea: Add some extra error that increases with the value of the coefficient

![[Pasted image 20210324192344.png]]

The extra error term is **shrinkage penalty**

- Lambda is called the tuning parameter
- Larger lambda is, the penalty gets higher
- As coefficient estimates near 0, penalty is very low
- So, as lambda increases, more coefficients move towards 0

L2 Norm

![[Pasted image 20210324192945.png]]

> Ridge regression requires scaling the features because the coefficients are all put together in the penalty term. Different scales for different coefficients can cause false penalties.

Standardization:

![[Pasted image 20210324193312.png]]

### Bias variance tradeoff
- As lambda increases, shrinking increases => variance decreases, bias increases slightly

### Drawback
- Do not select predictors as coefficients are close 0, but not 0
- So, all p predictors are included in final model

## Lasso regression

Idea: Like ridge, but makes coefficients 0

![[Pasted image 20210324193737.png]]

- Lasso uses l1 penalty
- ![[Pasted image 20210324193810.png]]
- Shrinks towards 0
	- When lambda is large enough, makes coefficients exactly to 0
	- So, performs variable selection
- Creates sparse models

In sparse models, the lasso performs much better than ridge. Lasso might work better for small p.

## Selecting tuning parameter

- Use cross validation with a grid of lambda values

