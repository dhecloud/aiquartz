---
aliases: [GCN]
---

### [[SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS]]
The layer wise propagation wise is defined as:
$$H^{l+1} = \sigma(\tilde{D}^{-\frac{1}{2} }\tilde{A}\tilde{D}^{-\frac{1}{2}} H^{(l)}W^{(l)})$$ where
1. $\tilde{A} = A + I_N$ is the [[Adjacency Matrix]] of the [[Undirected]] graph $G$ with added self connections
2. $I_N$ is the identify matrix
3. $\tilde{D}_{ii} = \sum_j \tilde{A}_{ij}$, $W^{(l)}$ is a layer specific trainable weight matrix
4. $\sigma(\cdot)$ is an [[Activation Function]]
5. $H^{(l)} \in \mathbb{R}^{N \times D}$ is the matrix of activations

Several definitions: 
1. ![[Spectral Graph Convolutions#SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering]] ^de1126
2. Linear model with $K=1$ and $\lambda_{max} \approx 2$ which results in $g_\theta^\prime \star x \approx \theta^\prime_0 x - \theta^\prime_1D^{-\frac{1}{2}}AD^{-\frac{1}{2}}$ ^41aec7
3. (final generalized form) $Z = \tilde{D}^{-\frac{1}{2}}\tilde{A}\tilde{D}^{-\frac{1}{2}}X\Theta$ where $\Theta \in \mathbb{R}^{C \times F}$ is a matrix of filter parameters and $Z \in \mathbb{R}^{N \times F}$ is the convolved signal matrix. This has a [[Complexity]] of $O(|E|FC)$ ^e0c9b8