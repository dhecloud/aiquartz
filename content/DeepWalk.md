This algorithm was presented in 2014 and is an well-established algorithm for [[Graph Neural Networks]]. It consists of a mapping function, extractor, reconstructor, and objective.

1. The mapping function is simply a look up table which retreives a node's embedding given its index.

2. The [[Random Walk]] Based [[Node Co-occurrence]] [[Extractor]] is done by simply randomly walking from a node until a specified number $T$ of nodes are visited (length of $T$).
3. Then, similar to the [[skip-gram]] algorithm, the [[Node Co-occurrence]] [[Reconstructor]] assigns a center node and the relative context nodes, and then calculates the probabilities $p(v_{con}|v_{cen}) = softmax(v_{con},v_{cen})$ 
4. Then the objective function is simply the negative log likelihood of the [[Softmax]] (similar to [[N-grams]]) to modify the embeddings

However, the [[Softmax]] is known to be a computational bottleneck, hence two main techniques have been employed: [[Hierarchical Softmax]] and [[Negative Sampling]].