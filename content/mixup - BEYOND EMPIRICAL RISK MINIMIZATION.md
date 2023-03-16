Author(s): [[Hongyi Zhang]], [[Moustapha Cisse]], [[Yann N. Dauphin]], [[David Lopez-Paz]]
Tags: #academic_papers
Read on: [[April 27th 2021]]
URL: https://arxiv.org/abs/1710.09412
# Main Contribution(s)
Proposees [[Mixup]], a data augmentation tactic for [[Classification]]
# Summary
[[Empirical Risk Minimization]] refers to minimizing the average error over the training data. Convergence of [[Empirical Risk Minimization|EMR]] is guaranteed as long as the size of the learning machine does not increase with the number of training data.

[[Vicinal Risk Minimization]] on the other hand refers to using data augmentation to describe a vicinity or neighborhood around each example in the training data

[[Mixup]] extends the training distribution by incoporating the **prior knowledge that linear interpolations of feature vectors should lead to linear interpolation of the associated targets**. [[Mixup]] has been shown to increase robustness of neural networks when learning from ocrrupt labels, facing adversarial examples, and improve generalization on speech, tabular and stablize the training of [[Generative Adversarial Network|GAN]]s.

Some reason why [[Mixup]] works:
1. Reduces amount of undesirable oscillations when prediction outside training examples
2. Linearity is a good inductive bias from the perspective of [[Occam's Razor]]
3. ![[Pasted image 20210427144419.png]] Leads to decision boundaries that are smoother (more generalized)


# Learning Gaps/Thoughts
# Simplify/Analogies