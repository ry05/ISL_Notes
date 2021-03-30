# Hypothesis Testing

A hypothesis is basically a guess. It's a guess that you make from the top of your head or based on observation or based on some cognitive trigger. But if you hypothesize, its also your responsibility to test the same.

> If you hypothesize, its also your responsibility to test it.

## A common hypothesis test

The null hypothesis test based on a simple linear regression model [[Single Linear Regression]]

H0 : The **null hypothesis** - X and Y are not related (Slope = 0)
HA : The **alternative hypothesis** - X and Y are related (Slope not 0)

Mathematically,

$$H0: \beta_1 = 0$$
$$HA: \beta_1 \neq 0$$

### Steps to test the null hypothesis

Step 1. Compute a test statistic (t-statistic)

$$t = \frac{\widehat{\beta_1} - 0}{SE(\beta_1)}$$

This will have a t-distribution (similar to a normal random variable) with (n-2) degrees of freedom.

Step 2. Calculate the p-value

The p-value is the probability of observing any value equal to absolute value of t or larger. 

The p-value is always confusing! Let's clear it up for once and for all.

![[Pasted image 20210322211456.png]]

**Interpret the t-statistic and p-value for TV**  
The probability/chance of seeing this data (17.67 t-statistic) under the null hypothesis assumption that *there is no relation between X and Y* is very, very low (<0.0001). 

In layman's terms, it means that if X and Y have no relation, then observing a data point that affirms this relation is highly unlikely.

In a more basic sense, *chance will play very little role* in making us observe a phenomenon that is not supposed to happen based on our assumption.

> If null is rejected, CI will not contain 0.

