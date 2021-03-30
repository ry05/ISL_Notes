# What is Statistical Learning?

After the super-light intro in [[Intro to SL]], it is time to dive a bit deeper.

![[Pasted image 20210322142247.png]]

There are 3 scatterplots, each depicting some kind of a relationship between the X and Y axis(Sales is the common Y axis). The blue line looks like an **estimate** of the direction in which the points are oriented.

A reasonable **model** of this data is

$$Sales \approx f(TV, Radio, Newspaper)$$

Read this as Sales is *dependent on amounts spent on TV, Radio and Newspaper advertisements*

Check notation on [[Notations]]. 

## Why model it like this?
There are 2 main advantages of modeling data using the above equation
- Helps make predictions about the future based on what we already know
- Helps infer the effect of certain variables on other variables in our data

![[Pasted image 20210322144955.png]]

The red curve is the **regression function**. It is as follows
$$f(x_{i}) = E(Y|X=x_{i})$$

Also called the **Expected value**. This is nothing but the average of all corresponding Y values for the given x_i value.

## The regression equation and errors

For some training data X, it is
$$f(X) = E(Y|X_1=x_{1}, X_2=x_{2}, X_3=x_{3}, X_p=x_{p})$$

The **ideal or optimal** predictor model of Y minimizes error.

Epsilon is the **irreducible error**

$$E(Y-\widehat{Y})^2 = E(f(X) + \epsilon -\widehat{f(X)})^2$$
$$=[f(X) - \widehat{f(X)}]^2 + Var(\epsilon)$$

The first term is **reducible error** - Can be reduced with a better model!  
The second terms is **irreducible** - Will exist as it is implicit to the way the data is collected.

## Will you be my neighbor?

Not always possible to get points where X = x_i 

![[Pasted image 20210322150337.png]]

In this case, average all points in the neighborhood of x_i. Called the **nearest neighbor** or **local averaging** method. 

The idea is to keep sliding this neighborhood across the X axis and keep estimating points to get the curve.

Neighbor method works when p<=4 and large N.

But, what if p is large? Enters the **curse** - The curse of dimensionality.

![[Pasted image 20210322151022.png]]

It's evident from the figure above that as p increases, the volume of the space enclosing the data increases while the data remains same(10% in this case). 

Think about it this way. Which of the two cases are harder?

a) Trying to shoot a duck moving around in an enclosure of 1 cubic meter
b) Trying to shoot a similar duck moving around in an enclosure of 10 cubic meter

Case b) exhibits the curse of dimensionality.

There are two kinds of models
- [[Parametric Models]]
- [[Non-parametric Models]]


