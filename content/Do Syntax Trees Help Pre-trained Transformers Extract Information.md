Author(s): [[Devendra Singh Sachan]], [[Yuhao Zhang]], [[Peng Qi]], [[William Hamilton]]
Tags: #academic_papers, #BERT, #Graph_Neural_Networks,
Read on: [[January 5th 2021]]
URL: https://arxiv.org/abs/2008.09084
# Main Contribution(s)
Incoporates [[Syntax Tree]]s using [[Graph Neural Networks|GNN]] into pretrained [[Transformer]] models to perform [[Semantic Role Labeling]], [[Named Entity Recognition|NER]], [[Relation Extraction]].
# Summary
As [[BERT]] models take in input subwords instead of linguistic tokens. To deal with subwords, new edges are added from the first subword to the remaining subwords of the same token.

![[Pasted image 20210105184046.png]] Two ways of incorporating the information; one by using the output embeddings of the [[BERT]] model, and the other by incorporating it into the [[Multi-Head Self-Attention]]. [[Syntax-GNN]] is used to learn the syntactic information

![[Pasted image 20210105185133.png]] ![[Pasted image 20210105185458.png]][[Semantic Role Labeling]], [[Named Entity Recognition|NER]], [[Relation Extraction]] results on [[CoNLL-2005 WSJ]], [[OntoNotes-5.0]], [[CoNLL-2012]], [[TACRED]], 

### Comparing gold parses and off-the-shelf parses
Using off the shelf parses provides little to no gains in [[F1 score]] for [[Semantic Role Labeling]]. For [[Named Entity Recognition|NER]], using gold parses does not yield substantial gain. **Substantial gains only observed in settings where gold parses are used.**

### Generalizing to [[BERT]] variants
![[Pasted image 20210105190055.png]]The gains from the Late Fusion model generalize to other widely used pre-trained transformer models.
# Learning Gaps/Thoughts
# Simplify/Analogies