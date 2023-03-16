Author(s): [[Eric Jang]], [[Shixiang Gu]], [[Ben Poole]]
Tags: #academic_papers
Read on: [[May 1st 2021]]
URL:  https://arxiv.org/abs/1611.01144
# Main Contribution(s)
Problem: Backpropagation cannot be done through samples
Solution: [[Gumbel-Softmax]] is a reparameterization trick that allows gradients to propagate through a differentiable sample
# Summary
![[Pasted image 20210501175347.png]]The [[Gumbel-Max trick]] draws samples from a [[Gumbel Distribution]]
![[Pasted image 20210501175500.png]] $k$-dimensional samples are generated and then used to approximate the density of the distribution ![[Pasted image 20210501175726.png]]
# Learning Gaps/Thoughts
# Simplify/Analogies