# Single Linear Regression

Linear regression is an algorithm for a supervised learning task that assumes that the dependence of the outcome (Y) to the predictor vector (X) is linear. Look at the Advertising and Sales figure in [[Statistical Learning]]

Linear regression is simple, yet very effective.

## Questions a regression model can help answer
- Are there relationships between the data? How strong?
- Is the relationship linear?
- Which predictors affect the target the most?
- Is their synergy between predictors?

## Model (Single predictor X and target Y)

$$Y = \beta_0 + \beta_1X + \epsilon$$

Beta_0 is the y-intercept.  
Beta_1 is the slope.  
Epsilon is the error term.  

Predicted target is represented as

 $$\widehat{y} = \widehat{\beta_0} + \widehat{\beta_1}x$$
 
 
## Estimating the parameters - Fitting

Fitting or training any parametric model has a singular objective: **Find a group of parameters so that the error is minimized**

The parameters in a linear regression are the beta coefficients. So, fitting means getting optimal values for them.

The error to minimize here is called Residual Sum of Squares(RSS).

$$RSS = e_1^2 + e_2^2 + ... + e_n^2$$

$$e_i = y_i - \widehat{y_i}$$

The parameters for a simple linear regression can be calculated as

![[Pasted image 20210322204937.png]]

- If slope is 0, there is no relation between the two variables

![[Pasted image 20210322205209.png]]

### Standard errors
From above equation its clear that
- More the variance of error, more the standard error => less precise the slope
- More spread out the X is, less standard error => more precise the slope

### Confidence intervals
Calculated from standard errors

> 95% CI means if 100 samples of a population were taken(each sample chosen with the exact same process), in 95 of those times the true value of the unknown parameter will lie in the 95% CI.

![[Pasted image 20210322205606.png]]

Assumption: Errors are normally distributed

There is a 95% chance that the true value of beta_1 (slope) is contained in the following interval=>

$$[\widehat{\beta_1} - 2.SE(\widehat{\beta_1}), \widehat{\beta_1} + 2.SE(\widehat{\beta_1})]$$

> It's important that the samples are taken with the exact same process for the CI to be accurate

Test the relationship between X and Y with [[Hypothesis Testing]]

### Overall accuracy of model

**Root Squared Error**

$$RSE = \surd{(\frac{RSS}{n-2})}$$

**R-squared**

$$R^2 = \frac{TSS - RSS}{TSS}$$

$$TSS = (y_i - \overline{y_i})^2$$

$$RSS = (y_i - \widehat{y_i})^2$$

- TSS is error of the simplest model to have => Null model error
- R^2 measures how much do we reduce TSS relative to itself. Or R2 measures how much variance the model can explain.
- In a simple linear regression setting, R^2 = r^2 where r is the correlation between X and Y

![[Pasted image 20210322212926.png]]

Higher the correlation => Higher the variance explained

**What is there are more predictors?** => [[Multiple Linear Regression]]








