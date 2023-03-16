---
aliases: [GIN, GINs]
---

### [[CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]

Networks with the aim of checking for [[Graph Isomorphism]] between a pair of graph. Formulated as:

$$f_{NN}(h_i^l, \{ h_j^l\}_{j \in N_i}) = (1+ \epsilon)g(h_i^l) + \sum_{j \in N_i}g(h_j^l)$$
where
1. Function $g$ must be [[Injective]]
2. A Sum [[Aggregator Functions|aggregator]]
3. $\epsilon$ must be irrational

A [[Feed-forward]] layer can approximate $g$ as the [[Universal Approximation Theorem]] guarantees the existence of such function