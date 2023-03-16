### [[Knowledge Graph Embeddings and Explainable AI]]
used to denote relationships that connect entities with literals, using an [[Ontology]]. [[Knowledge Graphs]]are often visualized using an [[Adjacency Matrix]] or tensor, where $T \in \mathbb{R}^{N\times R\times N}$ where $N$ is the number of entities and $R$ is the number of relationships. More specifically:
$$T_{i,j,k} = 
\begin{cases}
1 \text{ if } (e_i, r_jm e_k) \in \mathbb{G}  \\
0 \text{ otherwise } \\
\end{cases}$$