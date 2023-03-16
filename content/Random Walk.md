Formally defined as
$$p(v^{(t+1)}|v^{(t)}) = \begin{cases}
\frac{1}{d(v^{(t)})},& \text{if }v^{(t+1)}\in N(v^{(t)})\\
0,&\text{otherwise}
\end{cases}$$
where $d(v^{(t)})$ is the [[Degree]] of node $v^{t}$ and $N(v^{(t)})$ is the set of neighbours of node $v^{t}$.

In other words, a random node is chosen as the next node; without any bias; using a uniform distribution.