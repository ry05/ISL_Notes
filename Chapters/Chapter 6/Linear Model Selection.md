# Linear Model Selection

The linear model is simple and effective, but there are 2 main areas it can be improved:
- **Prediction accuracy**
	- As the difference between n and p gets lesser or if n < p, variance is too high(infinite in second case)
- **Interpretability**
	- If p is large, it is likely that many predictors have only negligible effects on the target
	- Having these predictors in the model only increases the complexity of the model for no great advantage
	- It' better to *remove these features* => set heir coefficient estimates to 0
	- Called **feature selection**

## Three methods
- [[Subset Selection]]
- [[Shrinkage]]
- [[Dimensionality Reduction]]


