---
aliases: [Admittance matrix, Kirchhoff matrix, discrete Laplacian, graph Laplacian]
---
# [Wikipedia](https://en.wikipedia.org/wiki/Laplacian_matrix)
Can be used to calculate number of [[Spanning Tree]]s for a graph. Can be used to construct low dimensional embeddings for [[Machine Learning]] applications.

 # On a [[Simple Graph]]
 A [[Laplacian Matrix]] of a [[Simple Graph]] is defined as $$L = D -A$$ where $D$ is a diagonal degree matrix $D = \text{diag}(d(v_1),...,d_(v_n))$, $A$ is its [[Adjacency Matrix]]. It be normalized in the form $$L = I - D^{-\frac{1}{2}}AD^{-\frac{1}{2}}$$. Intuitively, it measures how different the values of adjacent nodes are.
 - The [[Laplacian Matrix]] is [[Symmetric]] as both the [[Degree]] matrix and [[Adjacency Matrix]] is symmetric.

The [[Eigenvalue]]s of the [[Laplacian Matrix]] of a [[Simple Graph]] are non-negative.

The number of 0 [[Eigenvalue]] of its [[Laplacian Matrix]] of a [[Simple Graph]] equals to the number of [[Connected Component]] in the graph.

