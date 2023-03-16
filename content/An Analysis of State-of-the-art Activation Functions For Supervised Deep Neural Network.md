Author(s): [[Anh Nguyen]], [[Khoa Pham]], [[Dat Ngo]], [[Thanh Ngo]], [[Lam Pham]]
Tags: #academic_papers
Read on: [[31-May-2021]]
URL: [An Analysis of State-of-the-art Activation Functions For Supervised Deep Neural Network | DeepAI](https://deepai.org/publication/an-analysis-of-state-of-the-art-activation-functions-for-supervised-deep-neural-network)
# Main Contribution(s)
Problem: -
Solution: Provides an analysis of popular activation functions
# Summary
[[ReLU]] prevents vanishing gradients
[[ELU]] similar to [[ReLU]] except learning can happen when negative
[[SELU]] includes a form of normalization to map the map and variance of output at any layer in the network close to normal distribution using a scale constant
[[GELU]] includes the effect of dropout via a stochastic zero-one mask. This is needed because typical activation functions like [[ReLU]] cannot cover [[Dropout]] regularization
[[Inverse Square Root Linear Unit|ISRLU]] is a more efficient form of [[ELU]] as the exponential is replaced by a square root.

Experiments indicate that although [[ReLU]], [[ELU]], [[SELU]], [[GELU]] and [[Inverse Square Root Linear Unit|ISRLU]] can help to prevent vanished gradients or/and dead state issue, these activation functions should combine with other statistic layers such as Batch normalization or Dropout to further improve the ASC system performance
# Learning Gaps/Thoughts
# Simplify/Analogies