---
aliases: [GNN]
---

### [[CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]
##### Properties:
1. Rank-2 Tensors
2. Can be represented as list of edges (ideal for sparse graph), or a matrix.
3. [[Permutation Invariant]]

##### Impossibility Results and Bottlenecks
Cannot compute and learn some problems if the network capacity is limited.
1. Decision Problems: : Subgraph recognition, detecting cycles, subgraph is connected, etc
2. Optimization problems: [[NP-Hard]] problems, [[Polynomial-time]] problems
3. Estimation problems:  Computing graph diameter and girth

There is also a bottleneck in [[Aggregator Functions]], which is [[Over-Squashing]]. Bad news for tasks which require long range node interactions.

The solution to this is to include a [[Fully Connected Graph]] layer. 

### [[Relational inductive biases, deep learning, and graph networks]]
Notions like recursion, control flow, and conditional iteration are not straightforward to represent with graphs.