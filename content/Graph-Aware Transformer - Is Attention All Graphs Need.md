Author(s): [[Sanghyun Yoo]], [[Young-Seok Kim]], [[Kang Hyun Lee]], [[Kuhwan Jeong]], [[Junhwi Choi]], [[Hoshik Lee]], [[Young Sang Choi]]
Tags: #academic_papers, #Graph_Neural_Networks 
Read on: [[December 20th 2020]]
URL: https://arxiv.org/abs/2006.05213
# Main Contribution(s)
Proposes the [[GRaph-Aware Transformer]]
# Summary
The [[Transformer]] does not provide a way to explicitly encode the relational information between nodes. [[GRaph-Aware Transformer|GRAT]] aims to mitigate this using graphs as input.

![[GRaph-Aware Transformer#Graph-Aware Transformer - Is Attention All Graphs Need]]

Since the architecture is very similar to [[Transformer]]s, we can use [[BERT]]-style pretraining tasks, namely [[Masked Node and Edge Modelling]] and [[Graph Property Prediction]], which is modified from [[Masked Language Modelling]] and [[Next Sentence Prediction]].

### Experimental Results
![[Pasted image 20201220235220.png]] Results on [[QM9]], compared with [[Message-Passing Networks]] and [[DimeNet]]

![[Pasted image 20201220235543.png]] Results on [[USPTO]]
# Learning Gaps/Thoughts
# Simplify/Analogies