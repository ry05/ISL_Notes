# Random Forests

Idea: Similar to bagging, but *decorrelate trees*

## How is it done?
1. Like bagging, create B bootstrapped samples
2. For each split in the trees built, randomly choose only m predictors where m < p (usually ~root(p))
	1. Fresh selection of m predictors is taken at each split


> More trees, better chance for a predictor to make an appearance => Better accuracy


## Variable Importance
![[Pasted image 20210327101650.png]]
