# Support Vector Machines

Idea: Find a hyperplane that separates classes in feature space

## What if we can't find a hyperplane?
Then
- Soften what we mean by "separates"
- Enlarge feature space into higher dimensions so that separation is possible

## Hyperplane

Equation for a hyperplane in p dimensions is 

$$\beta_0 + \beta_1X_1 + \beta_2X_2 + ... + \beta_pX_p = 0$$

For p=2, hyperplane is a line
If beta_0 is 0, hyperplane goes through the origin

The vector 

$$\beta = (\beta_1, \beta_2, ..., \beta_p)$$ 

is the normal vector => Orthogonal to the surface of the hyperplane

![[Pasted image 20210327111327.png]]


## Maximal Margin Classifier
Of all the possible hyperplanes, find the one that maximizes the margin between the 2 classes.

![[Pasted image 20210327111352.png]]

But, for SVMs to work well, the data has to be **linearly separable**. SVMs also are affected by **noisy data**

## Non separable data

An approach is to *relax the idea of a separating hyperplane and allow for some misclassifications* => soft margin => way of regularization => decreases variance

![[Pasted image 20210327111945.png]]

C is the budget. As C gets bigger, the more stable the margin gets.

For SVM, standardization is important.

### Linear boundary fails. Then?

One approach is feature expansion. Add polynomial transformations of the predictors.

p dimensions to M dimensions => Easier to find a separating hyperplane

But, space gets bigger very fast!

An alternative is

### Kernels

![[Pasted image 20210327113030.png]]

![[Pasted image 20210327113048.png]]

> Alpha is non-zero for only points in the support vector set.

### What if K > 2

[[SVM for Multi-class]]


