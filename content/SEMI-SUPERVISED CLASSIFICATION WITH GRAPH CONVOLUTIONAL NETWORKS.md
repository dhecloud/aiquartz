Author(s): [[Thomas N. Kipf]], [[Max Welling]]
Tags: #academic_papers, #Graph_Neural_Networks
Read on: [[December 14th 2020]]
URL: https://arxiv.org/abs/1609.02907
# Main Contribution(s)
Proposes [[Graph Convolutional Network]], an efficient variant of [[Convolution Neural Network]]s which operate directly on graphs.
# Summary
![[Pasted image 20201215000925.png]]
Encode the graph structure directly using a [[Neural Network]] and train on a [[Semi-Supervised]] target. 
A simple and fast layer wise propagation rule is proposed: ![[Graph Convolutional Network#SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS]]

With the final approximation at ![[Spectral Graph Convolutions#SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS]], it is possible to stack multiple [[Graph Convolutional Network|layers]] followed by a non-linearity.
If $k=1$, the graph defaults to a linear function on the graph laplacian spectrum (1 neighbour away). We can thus create a linear formulation when we set $\lambda_{max} \approx 2$ at [[Graph Convolutional Network#^41aec7]] with 2 free parameters $\theta^\prime_0$ and $\theta^\prime_1$ with the filter parameters being able to be shared over the whole graph. 

The final form after using a renormalization trick is [[Graph Convolutional Network#^e0c9b8]]
Currently(at the time of writing), memory requirement grows linearly with the size of the dataset, and for large graphs do not fit in GPU memory. Mini-batches should take into account the number of layers in the model, as the K-th order neighbourhood for a [[Graph Convolutional Network|GCN]] with K layers has to be stored in memory for an exact procedure.

# Learning Gaps/Thoughts
# Simplify/Analogies