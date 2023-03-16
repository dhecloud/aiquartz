### Introduction
Classical [[Neural Network]]s cannot be easily generalized to graph-structured graph as the graph structure is not a regular grid. Essentially, [[Graph Neural Networks]] are a form of [[Representation learning]] on graphs. Typically, there is a [[Graph Filter]] operation which refines the node features, [[Activation Function]], [[Graph Pooling]] operation to reduce the number of nodes.

![[Pasted image 20201208174844.png]]![[Pasted image 20201208174855.png]]The general framework for both node focused and graph focused tasks are pretty similar, except that for graph focused tasks there are [[Graph Pooling]] operations and also multiple blocks

### [[Graph Filter]]s
There are two types: [[Spatial Graph Filtering]] and [[Spectral Graph Filtering]]

#### [[Spectral Graph Filtering]]
Goal is to modulate the frequencies of a graph signal such that some of its frequency are amplified and others are removed/diminished.

Given a graph signal, [[Graph Fourier Transform]] needs to applied to obtain its coefficients, then a filter will be applied, before reconstructing the signal using [[Inverse Graph Fourier Transform]]. However, we often do not know which frequencies/coefficients we should keep. Therefore, we mimic data-driven methods to learn the filter parameters.

The number of parameters to be learnt is dependent on the number of nodes, which can be extremely large. The filter is also likely a dense matrix and hence does not operate in a local spatial region. Hence, [[Poly-Filter]] is created to model the filter which a K-order truncated polynomial.

Other filters:
1. [[Cheby-Filter]]
2. [[GCN-Filter]]


#### [[Graph Filter]] for [[Multi-dimensional Graphs]]
The graph filter is applied individually to each input channel, then calculating the summation of the results.

#### [[Spatial Graph Filtering]]
The filtering operation is modelled by a parametric function, typically [[Feed-forward]] [[Neural Network]]s.  There are several architectures: [[GraphSAGE-Filter]], [[GAT-Filter]], [[ECC-Filter]], [[GGNN-Filter]], [[Mo-Filter]]

### [[Graph Pooling]]
[[Graph Filter]] operations are usually sufficient for node focused tasks. However, the graph focused tasks require the information to be summarized. There are two main kinds of information needed:
1. Node features
2. Graph Structure

There are two ways to do this:
1. Keep the more/most important nodes
2. Generate a new node representation

[[Flat Graph Pooling]]

#### [[Hierarchical Graph Pooling]]
These methods try to coarsen the graph using different methods

##### [[Downsampling-based Pooling]]
[[gPool]]

Information about unselected nodes are lost as nodes are discarded. 

### Supernode-based 
[[diffpool]]
[[EigenPooling]] 