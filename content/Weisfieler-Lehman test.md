---
aliases: [WL test, k-WL tests, k-Weisfieler-lehman test]
---

### [[CE7454 Deep Learning for Data Science Lecture Notes - Recent Developments in Graph Network Architectures]]
![[Pasted image 20201215215925.png]] Takes a pair (node, its neighborhood) (ie k=2) as input, and outputs a new color using a specified function. This function must be [[Injective]]. Results in a color histogram. If two graphs have the same color histogram, then they are **possibly** isomorphic.

Higher order interactions like hyperedges can allow us to use k > 2 tuples to model a test using [[Graph Neural Networks]]. A $k$-WL GNN can only find substructures consisting of $k$ or less nodes.

