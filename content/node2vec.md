Similar to [[DeepWalk]], but uses a biased second order [[Random Walk]]. The walk takes 2 parameters $p$ and $q$ is defined as: $$\alpha_{pq}(v^{(t+1)}|v^{(t-1)},v^{(t)} = \begin{cases}
\frac{1}{p},& \text{if dis}(v^{t-1},v^{t+1})=0\\
1,& \text{if dis}(v^{t-1},v^{t+1})=1\\
\frac{1}{q},& \text{if dis}(v^{t-1},v^{t+1})=2
\end{cases}$$ where $\text{if dis}(v^{t-1},v^{t+1})$ is the length of the shortest path between teh two nodes.