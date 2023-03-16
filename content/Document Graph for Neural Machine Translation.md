Author(s): [[Mingzhou Xu]], [[Liangyou Li]], [[Derek F. Wong]], [[Qun Liu]], [[Lidia S. Chao]]
Tags: #academic_papers, #Neural_Machine_Translation 
Read on: [[December 12th 2020]]
URL: https://arxiv.org/abs/2012.03477
# Main Contribution(s)
Uses [[Graph Neural Networks|GNN]]s to represent a document that connects relevant contexts regardless of their distances
# Summary
Long range memory has been a persistant problem. The authors aims to build a document graph for a document, where each word is directly connected to words which have a direct influence on its translation.
![[Pasted image 20201213022244.png]]
[[Graph Convolutional Network]] is used on the document graph and then fed to a [[Transformer]] model by additional attention and gating mechanisms. The gating mechanism is meant to dynamically control the influence of context information. Graphs used are directed, and [[Intra-sentential Relations]] and [[Inter-sentential Relations]] are constructed for the [[Graph Convolutional Network|GCN]]:
1. [[Adjacency]]
2. [[Dependency]]
3. [[Lexical Consistency]]
4. [[Coreference]]

## Experiments
![[Pasted image 20201213024453.png]]
[[BLEU]] scores on [[IWSLT En-Fr]], [[IWSLT Zh-En]], [[OpenSubtitles2018 En-Ru]], [[WMT19 En-De]]

## Analysis
Each kind of relation improves the translation quality.
Using a graph allows the model to connect a word with its contexts regardless of their distances in the document. A global context is benefict to **document level** [[Neural Machine Translation]].

# Learning Gaps/Thoughts
-
# Simplify/Analogies
-