Author(s): [[Sufeng Duan]], [[Hai Zhao]], [[Rui Wang]]
Tags: #academic_papers, #Neural_Machine_Translation, #Graph_Neural_Networks 
Read on: [[January 4th 2021]]
URL: https://arxiv.org/abs/2009.07489
# Main Contribution(s)
Proposes the [[Graph-Transformer]] by capturing information of subgraphs of different orders in every layer.
# Summary
![[Pasted image 20210104233210.png]]![[Pasted image 20210104234536.png]]Argues that a [[Simple Graph]] cannot effectively model all relationships between words, and hence proposes to view sentences as a [[Multi-dimensional Graphs]]. An edge is determined by the source node, the target node, the subgraph of the source node, and the subgraph of the target node.

![[Graph-Transformer#Graph-to-Sequence Neural Machine Translation]]

![[Pasted image 20210104234259.png]]Results on[[WMT14 En-De]], [[WMT14 De-En]]
# Learning Gaps/Thoughts
Paper was not really written well and thus i didnt really fully understand the idea 
# Simplify/Analogies