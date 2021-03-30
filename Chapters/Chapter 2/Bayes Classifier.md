# The Bayes Classifier

**Idea:** There exists a simple classifier that *assigns each observation to the most likely class, given its predictor values* and this classifier minimizes test error on average.

The success of this idea hinges on a few more definitions -

**Conditional probability**  
$$Pr(Y=j|X=x_0)$$

This is calculated as 
$$\frac{Pr(Y=j) \cup Pr(X=x_0)}{Pr(X=x0)}$$

But wait! How can you calculate that denominator? Worry not, here is an alternative (from [[Bayes Theorem]])

$$Pr(Y=j|X=x_0) = Pr(X=x_0|Y=j)\cdot\frac{Pr(Y=j) }{Pr(X=x0)}$$

*Much easier to compute!*

Probability of Y being j given that X is x_0  
In terms of the classification problem, a **conditional class probability** is as follows

$$p_{k}x = Pr(Y=k|X=x_i)$$

LHS means *probability that observation x belongs to class k*.

Probability that the **class** of a given **observation** is k when the observation is some x_i. For a binary classification problem, k can be 1 or 2.

The total number of classes is represented by **K**.

**The bayes optimal classifier**

An optimal classifier at X=x is

$$C(x) = j$$ if 
$$p_{j}x = max(p_{1}(x), p_{2}(x), p_{3}(x), ..., p_{K}(x))$$

**Simplified explanation**

1. Find the number of classes (K)
2. Calculate class conditional probability for each class
3. Find max
4. Assign the observation to the class with max value

> What sounds good => Great accuracy, very low error (using true conditional class probability)
> What can go wrong => Zero probability problem