Author(s): [[Alireza Mohammadshahi]], [[James Henderson]]
Tags: #academic_papers
Read on: [[January 13th 2021]] 
URL: https://arxiv.org/abs/2003.13118
# Main Contribution(s)
Proposes the [[Recursive Graph-to-Graph Transformer]] for [[Iterative Refinement]] of arbitary graphs and apply it to [[Dependency Parsing]]

# Summary
![[Recursive Graph-to-Graph Transformer#Recursive Non-Autoregressive Graph-to-Graph Transformer for Dependency Parsing with Iterative Refinement]]
[[Iterative Refinement]] is done by applying argmax indepedently to find the head of each node. Then the Maximum spannign tree algorithm is used to find the highest scoring valid dependency tree.

![[Pasted image 20210127170238.png]]![[Pasted image 20210127170405.png]]Evaluated on [[Universal Dependency Treebanks]], [[Penn Treebank]], and the [[German CoNLL 2009 Treebank]]

3 iterations of refinement achieve more than enough improvements than one iteration.
# Learning Gaps/Thoughts
# Simplify/Analogies