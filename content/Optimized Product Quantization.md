Author(s): [[Tiezheng Ge]], [[Kaiming He]], [[Qifa Ke]], [[Jian Sun]]
Tags: #academic_papers
Read on: [[May 1st 2021]]
URL: http://kaiminghe.com/cvpr13/index.html
# Main Contribution(s)
Problem: [[Product Quantization]] is not optimized yet in terms of performance 
Solution: Minimizes quantization distortions by 1. breaking down the solution into a smaller problem, 2. basing on a Guassian assumption
# Summary
[[Product Quantization]] aims to decompose the high-dimensional vector space into the Cartesian product of subspaces and then quantize these subspaces separately. It is a solution to [[Vector Quantization]] when an exponentially large number of codewords are desired, while requiring a lower memory cost. However, the optimal decomposition of the vector space is unaddressed. 

There are two approahces. 

### 1st approach: Non-parametric solution
Does not assume any data distribution. ![[Pasted image 20210501162305.png]]

### 2nd approach: Parametric solution
Assumes a parametric Gaussian distribution
# Learning Gaps/Thoughts
Glossed over many of the theory, too out of the water for me
# Simplify/Analogies 