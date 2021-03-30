# Problems with Linear Models

A few problems with linear models are as follows:

|Problem|Idea|Diagnosing|Solution|
|---|---|---|---|
|Non-linearity of response-predictor relationship|Underfit as linear model can't account for non-linear relationships|Use residual plots; if pattern emerges, then non-linear|Add non-linear transformations of predictors|
|Correlation of error terms|Estimated SE will be less than true SE, reducing p-value, thus giving a false sense of confidence|Residual plots against time for time-series data|Good experimental design|
|Heteroscedasticity|Non-constant variance of error terms; errors depend on outcome of model|Residual plots; if there is a funnel or non-uniform variance, then heteroscedastic|Transform the target with a concave function like log|
|Outliers|Target is far away from other point's targets|Scatter plot or studentized residuals|Remove outlier|
|High leverage points|Outliers, but for the predictor features|Scatter plot or studentized residuals; compute leverage statistic|Remove high leverage point|
|Collinearity|Relation between predictor|Correlation map, variance inflation factor|Remove features or group features|


