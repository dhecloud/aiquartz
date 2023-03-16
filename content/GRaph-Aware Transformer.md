---
aliases: [GRAT]
---

### [[Graph-Aware Transformer - Is Attention All Graphs Need]]
![[Pasted image 20201220233001.png]]The [[Transformer]] is modifed to take graphs as input. Each node is treated as a token. There is a a two path decoding step:
1. Encoding Path. Encodes the sub-graph and outputs the nodes' reprsentation. 
2. Node-and-Edge Generation Path. Inputs a special token `<G>` and outputs its node representation, and the label $l_i$ of the new node, computed as: $$l_i= \arg \max(f_l(h_i^\prime))$$ $$e_{ij}= \arg \max(f_e(f_p(h_i^\prime),f_p(h_j)))$$ where $h_j$ is the representation of the j-th node, $f_l$, $f_p$   and $f_e$ are [[Feed-forward]] layers. $f_p$ is used to reduce the dimension of each node 

The decoding process ends when the predicted label is `<EOG>`.