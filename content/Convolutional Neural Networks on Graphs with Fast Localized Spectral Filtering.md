Author(s): [[Michaël Defferrard]], [[Xavier Bresson]], [[Pierre Vandergheynst]]
Tags: #academic_papers, #Graph_Neural_Networks 
Read on: [[December 15th 2020]]
URL: https://arxiv.org/abs/1606.09375
# Main Contribution(s)
Provides a formulation of [[Convolution Neural Network]]s for [[Graph Neural Networks|GNN]] using [[Spectral Graph Theory]].
# Summary
### Formulation of [[Graph Convolutional Network]]
One major bottleneck of generalizing [[Convolution Neural Network|CNN]] to graphs is that the convolution and pooling operators are only defined for regular grids and not graph structures. Spatial approaches are easier but there is a challenge of matching local neighborhoods. On the other hand, [[Spectral Graph Filtering]] is already well defined using a [[Kronecker Delta]], though this operation is not naturally localized and is costly due to the $O(n^2)$ multiplication. These shortcomings can be overcome with a special choice of filter parameterization. Therefore a ![[Graph Convolutional Network#^de1126]] where the [[Chebyshev Polynomial]] is used to approximate kernels is formulated. There is another potential approximation, the [[Lanczos algorithm]], but this is more convoluted and is left up to future work.

### Formulation of [[Graph Pooling]]
![[Graph Pooling#Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering]]

### Experiments
#### [[MNIST]] 
28x28 image - 8-NN graph of the 2D grid which produces a graph of $n = |V| = 976$ nodes ($28^2 = 784$ pixels and 192 fake nodes as explained in Section 2.3) and $|E|$ = 3198 edges

#### [[20NEWS]]
16-NN graph where $z_i$ is the word2vec embedding of word, which produced a graph of $n = |V| = 10, 000$ nodes and $|E| = 132834$ edges

#### Comparison between [[Spectral Graph Filtering]] and Computational Efficiency
![[Pasted image 20201215151825.png]] Low computational complexity of the model which scales as $O(n)$.

#### Influence of Graph Quality
The statistical assumptions of locality, stationarity, and compositionality regarding the data must be fulfilled on the graph where the data resides. 
Experiments show that a simple k-NN graph of the grid is good enough to recover almost exactly the performance of standard CNNs. **Value of k does not have a strong influence on the results.**

# Learning Gaps/Thoughts
# Simplify/Analogies