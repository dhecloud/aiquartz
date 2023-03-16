Author(s): [[Saurabh Garg]], [[Sivaraman Balakrishnan]], [[J. Zico Kolter]], [[Zachary C. Lipton]]
Tags: #academic_papers
Read on: [[May 11th 2021]]
URL: https://arxiv.org/abs/2105.00303
# Main Contribution(s)
Problem: Current methods to induce generalization often lead to overparameterized models, or a reduction in training set
Solution: Proposes [[Randomly Assign, Train and Track]], which leverages unlabeled data
# Summary
Machine learning scientist establish generalization via:
1. Plugging in the empirical risk (performance on training data) to obtain a guarantee on the true risk (performance on practical cases)
2. Splitting data into training or holdout partitions

![[Pasted image 20210511133942.png]][[Randomly Assign, Train and Track|RATT]] shows that we can use randomly labeled data in our training and still achieve almost similar results. **The model can perfectly fit the clean portion of the data, so long as they fit the mislabeled data poorly**
# Learning Gaps/Thoughts
Interesting work
# Simplify/Analogies