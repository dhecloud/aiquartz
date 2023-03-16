Author(s): [[Petar Veličković]], [[Guillem Cucurull]], [[Arantxa Casanova]], [[Adriana Romero]], [[Pietro Liò]], [[Yoshua Bengio]]
Tags: #academic_papers, #Graph_Neural_Networks 
Read on: [[December 22nd 2020]]
URL: http://arxiv.org/abs/1710.10903
# Main Contribution(s)
Presents the [[Graph Attention Network]] which aims to address the shortcomings of convolutions
# Summary
Many tasks cannot be represented in a grid-like structure and lies in an irregular domain. These data can usually be representedusing graphs. [[Spectral Graph Convolutions]] depends on the [[Laplacian Matrix]] of [[Eigenvalue]]s, which depends on the graph structure. **This prevents a model trained on a specific structure from being applied to another graph structure**

[[Graph Attention Network]]s takes in a set of node features, and produces a new set of node features.  ![[Graph Attention#GRAPH ATTENTION NETWORKS Paper]]
### Experiments
![[Pasted image 20201222214033.png]] Results on [[Cora]], [[Citeseer]], [[Pubmed]], [[Protein-Protein Interaction data]].
# Learning Gaps/Thoughts
# Simplify/Analogies