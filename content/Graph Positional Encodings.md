### [[CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]
##### Properties:
1. Unique representation for each node.
2. Distance-sensitive : Nodes far apart on the graph should have different positional features
whereas nodes nearby have similar positional features.

##### [[Index Positional Encoding]]
![[Pasted image 20201215232712.png]]
Simplest possible way is to give an arbitary ordering to the nodes. Orderings are uniformly sampled from all possible choices so that the network will learn to be indepdent to these arbitrary choices.

##### [[Structural Message-Passing Networks]]

##### [[Laplacian Positional Encodings]]
Uses [[Spectral Graph Theory]] to obtain a [[Laplacian Matrix]]. 
Benefits of using Laplacian [[Eigenvector]]s as PEs:
1. Hybrid positional and structural encodings, invariant by index permutation
2. Unique and distance sensitive
3. Natural symmetries with the arbitary sign of eigenvectors
4. Graph generalizations of [[Transformer]]s' [[Positional Encodings]]