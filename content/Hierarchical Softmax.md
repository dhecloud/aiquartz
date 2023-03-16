![[Pasted image 20201204011202.png]]Nodes in a graph are assigned to the leaves of a [[Binary Tree]]. The probability $p(v_{con}|v_{cen})$ can be modelled through the path to the target node using a series of binary classifiers that takes the embedding vector of the center node.
For instance:
$$p(\text{left}|b0, v8) = \sigma(f_b(b_0)^T f(v_8))$$
Hence, in the above example, $p(v_3|v_8)$ $$ = p_{path}(b_1|v_8)\cdot p_{path}(b_4|v_8)\cdot p_{path}(v_3|v_8)$$$$= p(\text{left}|b_0,v_8) \cdot p(\text{right}|b_1,v_8)\cdot p(\text{left}|b_4,v_8)$$