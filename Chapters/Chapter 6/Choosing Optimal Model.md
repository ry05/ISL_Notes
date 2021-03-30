# Choosing Optimal Model

## Why not R2 or RSS?

- These measure training error, we need test error estimates
- Need better ways to compare across models with different number of predictors
	- Naturally, as predictors increase, RSS obviously decreases => This is not fair comparison as we will always choose the biggest model

### Adjusting training error to get estimate of test error

![[Pasted image 20210324191827.png]]

![[Pasted image 20210324192027.png]]

> The adjusted R2 is penalized for including unnecessary variables when compared to R2

