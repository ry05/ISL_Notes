# The Supervised Learning Problem

"Supervised" - Simply put, it means you have a "clear" idea of what you are looking to achieve in the problem. In more sophisticated terms as we might like it, supervised problems refer to problems that have data that is labeled. 

>Labeled does not only mean discrete labels. It can also refer to continuous values.

For notation, refer to [[Notations]]

## Learning! But how?

Cool! Now, let's revisit the concept of learning. How do we learn? A simple idea would be that
1. We first go over some material that we have, make associations with theory and application and add the information into our mental library
2. Then, we write a test to understand how effective our learning has been

A statistical learning problem works along similar lines. Step 1 is called **training** and step 2 is called **testing**.

Training data to a supervised problem is represented by a matrix (x<sub>1</sub>, y<sub>1</sub>),...,(x<sub>n</sub>, y<sub>n</sub>). 

## Objectives
1. Predict unseen test data
2. Understand which inputs affect the outcome
3. Measure quality of predictions

Point 2 is very important as it helps diagnose issues when predictions fail. The key at times might not be to get a model that can predict at 95% accuracy, but rather have a model that is also able to clearly explain why it does what it does.



