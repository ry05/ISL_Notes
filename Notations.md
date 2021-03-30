# Notations

## A basic learning model

**X** is used to refer to the vector of predictors.
$$X = (x1, x2, x3,..xp)$$

- The number of features/columns in X is represented by **p**
- The number of observations is represented by **n**

**Y** is used to refer to the target feature.

A simple supervised model can be written as
$$Y = f(X) + \epsilon$$

The **epsilon** represents the **error term**. The error captures measurement errors and any other discrepancies.

The predicted outcome is represented as $$\widehat{Y}$$

Therefore, any error (i.e the deviation of the prediction from the actual value) is $$E = Y - \widehat{Y}$$

or you could write this as 
$$E = (Y - \widehat{Y})^2$$

>Squaring the error ensures that opposite signs don't cancel each other out

## Linear Model

$$f(X) = \beta_0 + \beta_1X_1 + \beta_2X_2 + ... + \beta_pX_p$$

## Error measures

### Regression

#### Mean Squared Error
$$MSE = Average((y_i - \widehat{f}(x_i))^2)$$

### Classification

#### Misclassification Error
$$Error = Average(I(y_i \neq \widehat{y}_i))$$






