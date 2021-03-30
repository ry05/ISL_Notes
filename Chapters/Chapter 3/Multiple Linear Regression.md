# Multiple Linear Regression

Regression with more than one predictor.

$$Y = \beta_0 + \beta_1X_1 + \beta_2X_2 + ... +\beta_pX_p + \epsilon$$

beta_j is the *average effect on Y for a unit increase in X_j, holding all other predictors fixed.

The sales analysis in [[Statistical Learning]] gets the equation

$$Sales = \beta_0 + \beta_1\cdot TV + \beta_2\cdot Newspaper + \beta_3\cdot Radio + \epsilon$$

In the multiple linear regression setting, we have a **hyperplane** instead of the **line** in linear regression.

## Estimation of parameters - Fit

Similar to linear regression.

## Interpreting regression coefficients

There is more than one predictor now. So, it becomes important to interpret the meaning behind these coefficients.

- A coefficient of a predictor determines how much the target changes with a unit change in this predictor, holding all other predictors constant
	- But, this is completely true only if the *design is balanced* i.e *all predictors are uncorrelated*

> Avoid claims of causality for observational data

> *Essentially, all models are wrong, but some are useful* - George Box

> *The only way to find out what will happen when a complex system is disturbed is to disturb the system, not merely to observe it passively* - Mosteller and Tukey (paraphrasing George Box)

![[Pasted image 20210323093727.png]]

**Interpretations**
- Keeping radio and newspaper budget constant, changing the budget spent on TV by a single unit will improve sales by 0.046 units - This is statistically significant at the 5% level
- Radio and newspaper has a correlation of 0.35
- Newspaper's relation to sales is not statistically significant

So, a good idea would be to spend on TV and radio and drop newspaper.



