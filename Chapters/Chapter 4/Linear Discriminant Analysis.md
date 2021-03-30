# Linear Discriminant Analysis

## LDA when p = 1

The gaussian density function for a class k is

![[Pasted image 20210323182746.png]]

Assume that sigma_k (variance) is same for all classes.

Plugging the above equation into Bayes theorem and simplifying, we have

![[Pasted image 20210323183007.png]]

When K = 2 classes and both classes have prior probabilities of 0.5 (perfectly balanced), the decision boundary is at

$$x = \frac{\mu_1 + \mu_2}{2}$$

![[Pasted image 20210323183551.png]]

## LDA when p > 1

The gaussian density function for 2 variables is 

![[Pasted image 20210323184453.png]]

- the left has no correlation between x1 and x2
- the right has correlation between x1 and x2

The discriminant function is 

![[Pasted image 20210323184621.png]]

![[Pasted image 20210323185331.png]]

