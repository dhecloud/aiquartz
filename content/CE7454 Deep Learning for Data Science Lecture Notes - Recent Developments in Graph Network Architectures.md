Notes iteration: Semester 1 2020/21

# [[Graph Neural Networks]] based on the [[Weisfieler-Lehman test|WL test]]
![[Graph Isomorphism#CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]

This leads to the idea of turning the [[Weisfieler-Lehman test|WL test]] into a neural network. The task of determining [[Graph Isomorphism]] is not necessarily useful practically; but the **rich representation of data and graphs is extremely useful for downstream tasks**. 

The [[Aggregator Functions]] used must be [[Injective]]; to ensure an unique representation for the same input types, with a wide variety of encodings for distinct inputs. max, mean functions are not injective, but **sum** is. 

This leads to the formulation of ![[Graph Isomorphism Networks#CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]

[[Principal Neighbourhood Aggregation]] was also introduced as an generalization of the injective sum aggregator function to multiple aggregators with the degree-scalers

![[Graph Neural Networks#Properties]]
![[Equivariant Functions#CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]
These functions can be in the form of a function or a [[Feed-forward]] layer

[[Symmetric|Symmetry]] and [[Equivariant|Equivariance]] matters in [[Graph Neural Networks|GNN]] because they provide great inductive biases.

[[Weisfieler-Lehman test|k-WL tests]] originally had a $k$ value of 2, but with hyperedges and [[Graph Substructure Networks]] it is possible to go beyond 2. However, it increases the [[Complexity]] to $O(n^k)$ 
![[Pasted image 20201215230244.png]]It was proposed to multiply matrices to generate non-local interaction for a 3-[[Weisfieler-Lehman test|WL test]]. ![[Pasted image 20201215230249.png]] [[RingGNNs]] was also proposed to introduce higher-order interaction. [[Graph Low-Rank Global Attention]] was also introduced to further reduce the complexity while keeping the 3-[[Weisfieler-Lehman test|WL test]] expressivity power. 

# Expressivity and constraints

![[Pasted image 20201215231402.png]]

[[Graph Neural Networks|GNN]]s also adhere to the [[Universal Approximation Theorem]] and can inherently contain specific inductive biases, which can lead to strong generalization performances.

However, proof of existence does not mean that [[Stochastic Gradient Descent|SGD]] is guaranteed to find that solution.
![[Graph Neural Networks#Impossibility Results and Bottlenecks]]

[[Graph Isomorphism Networks|GINs]] are not able to differentiate representations of isomorphic nodes; it is assumed that they have the same representations. 
![[Graph Positional Encodings#CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]] was introduced to mitigate this limitation in expressivity. 

# [[Link Prediction]]
![[Pasted image 20201215233306.png]][[Graph Neural Networks|GNN]] can fail this task. It is mitigated by adding [[Node Positional Encodings]] and representing links as a joint representation of nodes.