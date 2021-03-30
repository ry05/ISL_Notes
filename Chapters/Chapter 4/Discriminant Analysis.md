# Discriminant Analysis

The idea is to model the distribution of X in each class separately and then use [[Bayes Theorem]] to flip things around and obtain Pr(Y|X). Usually, these distributions are **normal distributions**. 

In DA, Bayes theorem is rewritten as

![[Pasted image 20210323182033.png]]

## Why DA?
- When classes are well separated, log reg has unstable parameter estimates. DA does not get this.
- If n is sample and distribution of X is normal in each class, DA is more stable than log reg
- DA is better when K > 2 as compared to log reg
- DA uses Bayes theorem and as we know from [[Bayes Classifier]], this is the most ideal classifier

## Types of DA

- [[Linear Discriminant Analysis]]
- [[Other forms of DA]]