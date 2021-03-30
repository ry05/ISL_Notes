# Bayes Theorem

$$Pr(A|B) = \frac{Pr(B|A).Pr(A)}{Pr(B)} $$

In terms of a classification problem, the above equation can be re-written as

$$Pr(Y=k|X=x) = \frac{Pr(X=k|Y=k).Pr(Y=k)}{Pr(X=x)}$$

Based on conditional independence model, Pr(X=x) is the **total probability** of the observation x. Total probability is given by

$$Pr(X=x) = Pr(X=x|Y=1).Pr(Y=1) + Pr(X=x|Y=2).Pr(Y=2) + ... + Pr(X=x|Y=K).Pr(Y=K)$$

**Some terminology**  
- Pr(Y=k) is **prior probability**