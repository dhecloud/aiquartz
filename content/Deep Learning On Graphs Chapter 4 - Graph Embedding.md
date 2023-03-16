[[Graph Embbedding]] aims to map each node in a given graph to a low dimensional vector representation. There are two perspectives to viewing the graph: the original node-edge graph structure, and the embedding domain where each node is a continuous vector.

## [[Graph Embbedding]] on [[Simple Graph]]
In this part, these [[Simple Graph]]s are [[Static]], [[Undirected]], [[Unsigned]], and [[Homogeneous]].

There are various properties these [[Graph Embbedding]]s try to preserve, such as [[Node Co-occurrence]], [[Structural Role]], [[Node Status]], [[Community Structure]].

### Preserving [[Node Co-occurrence]]
One of the most popular ways to extract [[Node Co-occurrence]] is to perform [[Random Walk]]s in the graph.

[[DeepWalk]]
[[Hierarchical Softmax]]
[[Negative Sampling]]
[[node2vec]]
[[Large-Scale Information Network Embedding (LINE)]]

### Perserving [[Structural Role]]
 ![[Pasted image 20201207194353.png]]Structure is important as some sets of nodes might be far apart but exhibit similar structure. Thus, a [[Degree]]-based method is used to measure pairwise structural role similarity. Likewise, there is an [[Extractor]], [[Reconstructor]], and a mapping function.
 
 [[Hierarchical Structural Similarity Measure]]  is used to quantify [[Structural Role]] in a graph.
 
 A $k$ layer graph can be built from the weight of the edges between nodes: $$w_k(u,v) = \exp(-g_k(u,v))$$
 This design ensures that a node has a strong connection to the next layer if it is very similar to other nodes in the current layer. Hence, the [[Random Walk]] is more likely to be guided to the next layer.
 
 [[Reconstructor]] involves using a [[Biased Random Walk]]: $$p_k(v|u)=\frac{\exp(-g_k(v,u))}{Z_k(u)}$$ where $Z_k(u)$ is a normalization factor for the node $u$ in the layer $k$, defined as $$Z_k(u) = \sum_{(v,u)\in E_k}\exp(-g_k(v,u))$$.
 
 ### Preserving [[Node Status]]
 
 Refers to information like centrality. There are two components
 1. [[Node Co-occurrence]] information. Similar to that in [[DeepWalk]]
 2. Global status

Some methods try to learn both jointly. In this part we will focus on preserving only the global status ranking.

The [[Extractor]] calculates the global status scores using any of the [[Degree Centrality]] methods, and then order the nodes in descending order.

The [[Reconstructor]] recovers the global ranking information by modeling $$p_{global} = \prod_{1\leq j \leq N }p(v_{(i)},v_{(j)})$$ where $p(v_{(i)},v_{(j)}) = \sigma(w^T(u_{(i)}-u_{j}))$, which is the probability that node $v_{(i)}$ is ranked before $v_{(j)}$. The [[Reconstruction Loss]] is thus $$L_{global} = -\log(p_{global})$$

### Preserving [[Community Structure]]
There are two types of information:
1. pairwise connectivity information
2. Similarity between neighborhoods of nodes.

#### Node-oriented structure
The [[Extractor]] computes the pairwise neighborhood similarity (both information) using $$s_{i,j} = \frac{A_iA_j^T}{||A_i||||A_j||}$$ where $A_i$ is the i-th row of the adjacency matrix.

[[Reconstructor]] linearly combines both types of information $A$ and $S$. $$P = A + \eta\cdot S$$ where $\eta > 0$ controls the importance of the neighborhood similarity. The [[Reconstruction Loss]] is $L(W_{con}, W_{cen}) = || P - W_{con}W_{cen}^T||^2_F$

#### Community Structure
Uses [[Modularity Maximization]]

### [[Graph Embbedding]] on Complex Graph

#### [[Graph Embbedding]] for [[Heterogeneous Graphs]]

[[Heterogeneous Network Embedding (HNE)]] uses different deep models for different type of nodes. For example, [[Convolution Neural Network]] for image nodes.

The [[Extractor]] extract node pairs with edges as the information using an [[Adjacency Matrix]] $A$. The [[Reconstructor]] aims to recovers the $A$. The [[Reconstruction Loss]] is a [[cross entropy]] loss.

The [[Meta-Path Schema]] exists in a [[Heterogeneous Graphs]] to guide a [[Random Walk]] according to the type of node and edge.

#### [[Graph Embbedding]] for [[Bipartite Graphs]]

[[Bipartite Network Embedding (BiNE)]] induces two [[Homogeneous]] graph and extracts [[Node Co-occurrence]] in the same way as [[DeepWalk]]

#### [[Graph Embbedding]] for [[Multi-dimensional Graphs]]

Aims to learn two things:
1. General node representation
2. Dimension specific representation

These representations are not indepedent and hence it is important to explicit model their dependence. $$u_{d,i} = u_i + r_{d,i}$$ where $u_i$ is the general representation and $r_{d,i}$ is the representation capturing the independent information of dimension $d$.

#### [[Graph Embbedding]] for [[Signed Graphs]].
Nodes should be closer to nodes with positive edges than their negative edges. 

[[Extractor]] extracts a triple nodes $(v_i, v_j, v_k)$ of positive node, center node, negative node. However, the cost of forming negative edges is higher than positive edges. Therefore, a virtual node is created to artifically create negative edges between each node. The [[Reconstructor]] aims to reconstruct the information of a given triple by infering the relative relations of the triple based on the node embeddings.

#### [[Graph Embbedding]] for [[Hypergraphs]]

[[Dynamic Heterogeneous Network Embedding (DHNE)]] aims to learn to types of information:
1. Proximity described directly by hyperedges.
2. [[Node Co-occurrence]]

The frequency for which a pair of nodes co-occur in hyperedges indicates how strong their relation is.


#### [[Graph Embbedding]] for [[Dynamic Graphs]]

[[Temporal Neighbors]] in [[Dynamic Graphs]] are nodes connected with a node after time $t$. 
[[Temporal Random Walk]]