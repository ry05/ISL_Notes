# Extensions of the Linear Model

## Qualitative predictors

Check [[Important Questions on Regression]]

## Interactions

Removing the additive assumption

When predictor variables have an effect on each other and not just with the target.

In marketing, this **interaction** is called as the **synergy effect**

![[Pasted image 20210323100902.png]]

- Coefficient of TV has now changed to include the value of radio

![[Pasted image 20210323101228.png]]

> **Hierarchy principle**: If we include an interaction in a model, we should also include the main effects, even if associated p-values are not significant
> It's hard to interpret interaction terms without the main effects

### Between qual. and quant. predictors

Similar to qualitative predictors and interaction terms

![[Pasted image 20210323101719.png]]

Left: No interaction between student and income
- As income increases, credit card balance increases 

Right: Interaction between student and income
- As income increases, credit card balance increases, but
	- This increase is sharper for non-students than it is for students

## Non-linear effects of predictors

![[Pasted image 20210323101957.png]]

> The model is still "linear" as coefficients are linear. Only the predictors are non-linear

### Disadvantages
- Hard to interpret
- Higher degree polynomials can lead to overfitting

The next thing to know are about problems with the linear model - [[Potential Problems]]