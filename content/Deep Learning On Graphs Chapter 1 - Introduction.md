# Introduction
### Reasons to learn [[Deep Learning on Graphs]]:
1. Many datasets can be representated explicitly as a graph
2. A vast number of real world problems can be addressed as a small set of computation tasks on graphs. These include [[Link Prediction]]

### Obstacles
Traditional [[Machine Learning]] tactics cannot be applied directly on graphs. However, the advent of deep methods allows for [[Representation learning]] which presents unprecedented opportunities.

### Brief History
##### Feature Selection on Graphs
Aims to automatically select a small subset of features with minimal redundancy but maximal relevance to the target.
##### Representation Learning on Graphs
Learns a new set of node features onto a low dimensional space so that other algorithms like [[K-means clustering]] can be used easily on it. However, preserving structural information is often computationally expensive.
* For example, the [[skip-gram]] model from [[word2vec]] is often used to learn node representation. [[DeepWalk]] treats each node as a word and generate sentences using [[Random Walk]].
##### [[Graph Neural Networks]]
Typically refers to using [[Neural Network]]s for [[Representation learning]]. There are two main approaches:
1. **Spatial**. Leverage on the structure of the graph
2. **Spectral**. Uses the [[Graph Fourier Transform]] and [[Inverse Graph Fourier Transform]].

Some interesting facts about [[Graph Neural Networks]]  :
1. To obtain a good graph representation, numerous [[Pooling]] methods have been introduced
2. They are vulnerable to [[adversarial attacks]], just like [[Neural Network]]s
3. [[Scalabilty]] is a problem
4. [[Auto-Encoders]], [[Recurrent Neural Networks]], [[Generative Adversarial Network]], [[Variational Auto-Encoder]] have been generalized successfully to graphs
5. Graphs are also an univeral data representation!
