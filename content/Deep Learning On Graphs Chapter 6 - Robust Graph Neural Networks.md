[[Graph Neural Networks]] inherit both advantages and disadvantages of traditional [[Neural Network]]s.

[[adversarial attacks]] fall into several attack types:
1. [[Evasion Attack]]
2. [[Poisoning Attack]]
These attacks can be done by:
1. Modifying Node Features
2. Adding or deleting edges
3. Injecting fake nodes

Attackers aim to either:
1. Directly attack a targeted node, or directly manipulate other nodes to influence the target node 
2. Simply attack the whole graph to lower the model's performance

Attackers can have several attack settings: 
1. [[White-box attack]]
2. [[Gray-box attack]]
3. [[Black-box attack]]

### [[White-box attack]]
Most methods use gradient information and formulate the attack as an optimization problem, or use the gradients to determine the effectiveness to modifying graph structure and features

Some examples:
1.  [[PGD Topology Attack]]
2. [[Integrated Gradient Guided Attack]]

### [[Gray-box attack]]
Usually does not directly attack the given model, but uses a surrogate model trained on the available training data as a proxy to attacking the deployed model.
1. [[Nettack]]
2. [[Metattack]]

### [[Black-box attack]]
Most methods try to adopt a reinforcement learning strategy

Some examples:
1. [[RL-S2V]]
2. [[ReWatt]]

### [[Graph Adversarial Defense]]
Types of defenses include:
1. [[Graph Adversarial Learning]]
    - [[GraphAT]]
	- Generating [[adversarial attacks]] for hidden representations
2. [[Graph Purification]]
	- Removing edges with low feature similarity based on a metric. For instance: [[Jaccard Similarity]]. 
	- Low-rank Approximation of Adjacency Matrix. Finds that [[Nettack]] tends to increase the [[Adjacency Matrix]]'s rank. Therefore [[Singular Value Decomposition]]
3. [[Graph Attention]]
    - [[RGCN-Filter]]
    - [[PA-GNN]]
4. [[Graph Structure Learning]]
    - [[Pro-GNN]]




