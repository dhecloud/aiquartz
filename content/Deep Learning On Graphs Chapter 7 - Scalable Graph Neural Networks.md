[[Graph Neural Networks]] suffers from severe scalability issue. [[Stochastic Gradient Descent]] is not as straightforward as training samples are still conneted to other labeled/unlabeled samples in the graph. [[Neighborhood Explosion]] is one of the problems as $O(deg^L\cdot d)$ memory is required to store the node reprsentations. Therefore, sampling is used to reduce the number of nodes. There are three main types of sampling:
[[Node-wise Sampling]], [[Layer-wise Sampling]], [[Subgraph-wise Sampling]].

### [[Node-wise Sampling]]
Approximate the expectation by [[Monte Carlo]] Sampling
[[GraphSAGE-Filter]] can also be viewed as a type of this method.
Still suffers from [[Neighborhood Explosion|Neighbourhood Expansion]]

### [[Layer-wise Sampling]]
[[Importance Sampling]] is used to design the methods.

### [[Subgraph-wise Sampling]]
[[Edge-based Sampler]]
[[RW-based Sampler]]