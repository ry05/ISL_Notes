# Parametric Models

Simple. Models that have parameters	that help estimate the data.

## Two steps
### Step 1. Make an assumption about the data's form or shape

- Is the data linear? Is it non-linear?

If the data is linear, we call the corresponding model a **linear model**.

$$f(X) = \beta_0 + \beta_1X_1 + \beta_2X_2 + ... + \beta_pX_p$$

To find f(X), the only task that is necessary is to find the values of the beta coefficients. Theses coefficients are **parameters**.

> For p features, there are (p+1) coefficients to estimate

### Step 2. Fit the model and find the values of the parameters

Fitting is done so as to minimize error

![[Pasted image 20210322152155.png]]

## Properties

- Easy to interpret
- Not very flexible
- Could be prone to **underfitting**

## Examples
- Linear models
- Basic SVM

