Author(s): [[Federico Bianchi]], [[Gaetano Rossiello]], [[Luca Constabello]], [[Matteo Palmonari]], [[Pasquale Minervini]]
Tags: #academic_papers, #Graph_Neural_Networks 
Read on: [[December 28th 2020]]
URL: https://arxiv.org/abs/2004.14843
# Main Contribution(s)
Provides a introduction and summary of [[Knowledge Graphs]] and [[Knowledge Graphs Embeddings]], and show how to generate and evaluate them.
# Summary
![[Knowledge Graphs#Knowledge Graph Embeddings and Explainable AI]]

![[Knowledge Graphs Embeddings#Definition]]
However, [[Knowledge Graphs]] usually have many observed facts and few axioms and rules, which means that much of the learning is not directly interpretable due to the lack of strict logical rules. However, it is possible to observe interactions between different entities by analyzing the structure of the graph.

![[TransE#Knowledge Graph Embeddings and Explainable AI]]
![[Description-Embodied Knowledge Representation Learning#Knowledge Graph Embeddings and Explainable AI]]

![[Pasted image 20201228203140.png]]

### Structure-based Embeddings
1. [[Translational Models#Knowledge Graph Embeddings and Explainable AI]]
2. [[Bilinear Models#Knowledge Graph Embeddings and Explainable AI]]
3. Neural Models, such as [[Convolution Neural Network]]s.

### Enhanced Knowledge Graph Embeddings
Approaches so far rely on triples which denote the pairwise relationship between entities. There are other types of embeddings:
1. [[Path]] Embeddings
2. Distributional Embeddings. Embeddings are represented by those models that view language under a distributional perspective in which the meaning. For example, [[word2vec]]
3. Text Enhanced Embeddings. Uses textual information to enhance the performance of [[Knowledge Graphs Embeddings]]
4. Image Enhanced Embeddings. Integrates images inside the scoring function
5. Logic Enhanced Embeddings. Combines logic and facts for knowledge representation.
6. Schema Aware Embeddings
7. Hyperbolic Embeddings
8. Temporal Knowledge Graph Embeddings.

### Evaluation
[[Link Prediction]] can be thought of the task to finding the entity to complete the triple $(h,r,?)$. [[Mean Reciprocal Rank]] is often used to evaluate this task.

### [[Explainability]] in [[Knowledge Graphs Embeddings]]
[[Knowledge Graphs Embeddings]] are often referred to as **sub-symbolic**, since they are elements in the vector space, but come from direct relationships with other entities. A methodology to effectively explain the predictions of [[Knowledge Graphs Embeddings]] is still not founded

An advantage of [[Knowledge Graphs Embeddings]] is that they come with a previous meaning; therefore they **do not inherit ambiguity** and thus be more effectively used for reasoning and explainable systems.
# Learning Gaps/Thoughts
# Simplify/Analogies