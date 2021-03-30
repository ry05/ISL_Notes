# Decision Trees

![[Pasted image 20210327083138.png]]

## The basics
- Decision trees have the following components
	- Root
	- Nodes
		- Internal nodes: Represent regions. A region can have one or more observations. These are split further
		- Terminal nodes: Represents regions which are not split any further
	- Branches

![[Pasted image 20210327083422.png]]

## Building trees for regression
1. Divide the predictor space into J distinct and non-overlapping regions where a region is represented by R_j, j in [1, J]
2. For each observation in R_j, predict the mean of all response values of observations in R_j
3. The goal: Minimise RSS

$$RSS=\sum_{j=1}^{J} \sum_{i \in R_j} (y_i-\widehat{y}_{R_j})^2$$

But the process above is computationally inefficient
- How many boxes would there be?
- Is it feasible to calculate RSS?

Improvements
- Top-down greedy approach
	- Make a split that is the *best option at the current node*
	- Best option is what brings about the greatest decrease in RSS
- Stop when **stopping criterion** is reached

## Making predictions
1. Just pass the point through the created decision tree
2. It will end up in a terminal node and thus get the corresponding value in that node
	1. In regression, this is the mean of all observations' responses in the node
	2. In classification, its the (major)label of observations in the node


## Pruning a tree
- Large trees increase the risk of overfitting

Idea: Grow a very large tree T_0 and then prune it back to get a subtree via cost complexity pruning or weakest link pruning

![[Pasted image 20210327085058.png]]

> Resembles shrinkage penalty idea

Alpha is a tuning parameters - Controls tradeoff between ubtree's complexity and its fit to training data
\T\ is the number of terminal nodes of the tree

![[Pasted image 20210327085313.png]]

![[Pasted image 20210327085748.png]]

As alpha increases, the tree is deeper.

## Classification trees

- Each observation to be predicted in a region(terminal node) is given the label of the most commonly occurring class

Instead of RSS, classification error rate is used

$$E=1-max_{k}(\widehat{p}_{mk})$$

Classification error rate is the probability of an observation not belonging to the most common class in the region Rm.

But, other measures are used.

### Gini measure

![[Pasted image 20210327093310.png]]

More Gini, more impurity => If G is 0, the node has only observations that belong to a single class

### Cross entropy

![[Pasted image 20210327093556.png]]

More entropy => more impurity

![Classification and Regression Trees](https://miro.medium.com/max/602/0*Nsuwaq2Padpbdz9Y.png)







