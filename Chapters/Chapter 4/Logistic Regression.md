# Logistic Regression

Consider a binary classification problem

$$p(X)=Pr(Y=1|X)$$

Logistic regression form

$$p(x) = \frac{e^{\beta_0 + \beta_1X}}{1+e^{\beta_0 + \beta_1X}}$$

e = 2.718

p(x) bounded between [0, 1]

Let's simplify the logistic regression form a bit more

$$p(x) = \frac{e^{linearmodel}}{1+e^{linearmodel}}$$

Rearranging a bit,

$$log(\frac{p(x)}{1-p(x)}) = \beta_0 + \beta_1X$$

This is called the logit pr log odds transformation of p(x).

Getting the beta parameters will help get the probabilities.

## Fitting - Maximum likelihood

Maximum likelihood is used to estimate the parameters. 

![[Pasted image 20210323152214.png]]

**Idea:**  
Find values for beta_0 and beta_1 such that the plugging these values into p(x) will yield a probability close to 1 for observations with target as 1 and close to 0 for those with target 0.

> Linear regression is a special type of maximum likelihood

> Take the units into consideration when checking coefficients

## Making predictions

Plug in beta values into the p(x) to find
$$\widehat{p(x)}$$

This was for simple logistic regression with only a single predictor. What if there is more than one predictor? => [[Multivariate Logistic Regression]]
