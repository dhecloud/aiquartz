### [[Deep Learning On Graphs Chapter 9 - Beyond GNNs, More Deep Models on Graphs]]
There are two types of autoencoders:

In (Wang et al., 2016), the model aims to reconstruct the rows of the [[Adjacency Matrix]] of the graph using a [[Feed-forward]] [[Neural Network]]. Minimizing the [[Reconstruction Loss]] will compress the neighborhood information into the low-dimensional representation. Due to the sparisty of the [[Adjacency Matrix]], it might cause overfitting to the 0 elements. Therefore, more penalty is imposed to the non-zero elements. This approach only focuses on the graph structure without involving the node features.

In (Kipf and Welling, 2016b), [[GCN-Filter]] is used to build the encoder with utilizes both the graph structure information and node features. The decoder reconstructs the graph which includes the [[Adjacency Matrix]] and attribute matrix. However, the authors only reconstructs the [[Adjacency Matrix]] in their approach.