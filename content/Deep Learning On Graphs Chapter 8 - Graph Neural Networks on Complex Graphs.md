skimmed through most of it.

[[Meta-Path Schema]] is used to split [[Heterogeneous Graphs]] into several [[Homogeneous]] [[Simple Graph]]. [[Graph Filter]]s are applied to these split graphs.

Two [[Graph Filter]]s are needed for 2 sets of nodes in [[Bipartite Graphs]]

For [[Multi-dimensional Graphs]], there are two types of neighbors, the [[Within-Dimension Neighbor]], and [[Across-Dimension Neighbor]]. Both types are aggregated into a node

The negative edges in [[Signed Graphs]] carry very different meaning from positive edges. A naive way would to be split the graph into either positive or negative graph. However, this ignores the complex interactions between positive and negative edges. Therefore, [[Balance Theory]] proposes to model the relations between the positive and negative edges using a specific graph filter designed for [[Signed Graphs]]. Information from balanced neighbors and unbalanced neighbors should be maintained separately as it means very different things.

Pairwise relations can be extracted from [[Hypergraphs]], which turns the graph into a [[Simple Graph]]. Then [[Graph Filter]]s for [[Simple Graph]]s can be applied.

[[EvolveGCN]] was proposed to tackle [[Dynamic Graphs]] by training $T$ models for $T$ snapshots.