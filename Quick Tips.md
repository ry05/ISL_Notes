# Quick Tips
Let's make our lives easier :)


## Data Analysis
- When you get some data, look at it before running it through some "fancy" algorithm

## Visualization
- Use a pair plot if `p` is not too large (let's say < 10) to identify relationships between the features
- Use color to distinguish between classes when using scatter plots for exploring a classification problem
- Use box plots to explore quantitative predictors and their effects on the target in classification problems

## Modeling
- Plot train and test errors
	- If the test error has a U-shape while train error keep decreasing, then your model is overfitting
- When writing equations, use the (hat) for all estimates
- In classification problems, try to classify to the prior. This is the baseline to beat
- Regularization options
	- ![[Pasted image 20210325113310.png]]