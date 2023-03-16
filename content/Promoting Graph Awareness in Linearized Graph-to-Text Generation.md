Author(s): [[Alexander Hoyle]], [[Ana Marasović]], [[Noah Smith]]
Tags: #academic_papers, #Graph_to_Text, #Graph_Neural_Networks 
Read on: [[January 7th 2021]]
URL: https://arxiv.org/abs/2012.15793
# Main Contribution(s)
Introduces the use of linearized graph inputs to pretrained [[Transformer]]s, and introduces several objectives.
# Summary
There are several ways of inputting a graph into a model
1. Form of tables
2. [[Resource Description Framework]]
3. [[Abstract Meaning Representations]]
5. [[Linearized Graph]]

Initially using [[Linearized Graph]] was outperformed by graph-based encoders, but with the advent of pretrained [[language model]]s its performance has taken off.

### To what extent is [[Transformer]] models invariant to [[Linearized Graph]]s? (paraphrased)
Linearized as [[Spanning Tree]] over graphs in [[PENMAN]] notation. This is basically sort of checking for [[Permutation Invariant|Permutation Invariance]] by doing some sort of data/graph augmentation.
![[Pasted image 20210107221337.png]]Results on [[AMR17]] and [[WebNLG]], suggest that **pretrained linearized models are not linearization-invariant**, failing to learn robust implicit graph representations even on [[WebNLG]]
### Does encouraging [[Transformer]] models to represent graph better lead to better generation?
Proposes [[Masked Graph Modelling]], similar to [[Masked Language Modelling]], and [[Graph Reordering]]. This is meant as a [[Scaffolding]] method; to help the model learn intermediate knowledge before the harder task.

![[Pasted image 20210107222618.png]]Results suggest that focusing on learning graph representation is still more importatnt. Standard [[Masked Language Modelling]] is less benefical than [[Masked Graph Modelling]], even though both outperforms the baseline 
# Learning Gaps/Thoughts
# Simplify/Analogies