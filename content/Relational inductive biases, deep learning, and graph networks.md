Author(s): [[Peter W. Battaglia]], [[Jessica B. Hamrick]], [[Victor Bapst]], [[Alvaro Sanchez-Gonzalez]], [[Vinicius Zambaldi]], [[Mateusz Malinowski]], [[Andrea Tacchetti]], [[David Raposo]], [[Adam Santoro]], [[Ryan Faulkner]], [[Caglar Gulcehre]], [[Francis Song]], [[Andrew Ballard]], [[Justin Gilmer]], [[George Dahl]], [[Ashish Vaswani]], [[Kelsey Allen]], [[Charles Nash]], [[Victoria Langston]], [[Chris Dyer]], [[Nicolas Heess]], [[Daan Wierstra]], [[Pushmeet Kohli]], [[Matt Botvinick]], [[Oriol Vinyals]], [[Yujia Li]], [[Razvan Pascanu]]
Tags: #academic_papers, #Graph_Neural_Networks , #critique 
Read on: [[December 16th 2020]]
URL: https://arxiv.org/abs/1806.01261
# Main Contribution(s)
Explore how relational inductive biases within deep learning architectures can facilitate learning about entities, relations, and rules. 
Discuss how graph networks can support relational reasoning and combinatorial reasoning.
# Summary
![[Inductive Biases#Relational inductive biases deep learning and graph networks]]
 Relational inductive biases are [[Inductive Biases]] which impose constraints on relationships and interactions among entities in a learning process.
 
 In this paper, we ask how each type of architecture support relational reasoning
 ![[Pasted image 20201216161014.png]]
 1. [[Feed-forward]] layers, or Fully connected layers, take in the full input signal. There is no reuse, no isolation of information. The [[Inductive Biases]] in this model is extremely weak
 2. [[Convolution Neural Network|Convolutional Layers]] take in grid elements or individual units. The benefits here are [[Locality Invariant]] or [[Translation Invariant]]. Very effective for image data because there is a high covariance within local neighborhoods which diminishes with distance.
 3. [[Recurrent Neural Networks|Recurrent layers]] contains [[Temporal Invariant]] 
 4. [[Graph Neural Networks|GNN]] are [[Permutation Invariant]] and supports arbitrary relational structures. 

![[Pasted image 20201216162206.png]]Different types of input data being represented as a graph.

![[Pasted image 20201216162259.png]] Different variations of block structures for [[Graph Neural Networks|GNN]]. 

As noted in [[Graph Neural Networks#Impossibility Results and Bottlenecks]], there are several limitations ![[Graph Neural Networks#Relational inductive biases deep learning and graph networks]]
# Learning Gaps/Thoughts
# Simplify/Analogies