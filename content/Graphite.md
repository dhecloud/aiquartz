### [[Graphite - Iterative Generative Modeling of Graphs]]
Combines [[Probabilistic Modeling]] and [[Representation learning]] for Graphs.

![[Pasted image 20201222030547.png]]Aims to learn a parameterized distribution over [[Adjacency Matrix]]s. Aims to do only [[Graph Structure Learning]], and any other information is used as conditioning evidence.

Encoding is done to get the mean and standard deviation using a [[Graph Neural Networks|GNN]] which takes in [[Adjacency Matrix]] and X as inputs. 

Decoding is done via two steps:
1. Constructs an intermediate weighted graph
2. Passes a pass through a parameterized [[Graph Neural Networks|GNN]]

The [[Associative]] properity of matrix multiplication is also used as a trick to perform right multiplication which is a faster and shorter way.

[[Graphite-VAE]] and [[Graphite-AE]] are two different models used. 
**refer to paper for full details, this is super simplified**