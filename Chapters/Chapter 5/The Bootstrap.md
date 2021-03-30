# The Bootstrap

Used to quantify uncertainty associated with a given estimator. The bootstrap can be used to estimate the standard errors of the coefficients from a linear regression fit.

Idea: Repeatedly sample *with replacement* B times from a dataset of n observations such that each sample has n observations and compute error estimates with each sample and aggregate for final estimate.

![[Pasted image 20210324113429.png]]

![[Pasted image 20210324113526.png]]

Bootstrap *does not work well with prediction error estimation* due to the significant overlap of observations in the bootstrap data.


