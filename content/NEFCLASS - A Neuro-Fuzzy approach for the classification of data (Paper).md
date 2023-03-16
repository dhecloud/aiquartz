Author(s): [[Detlef Nauck]], [[Rudolf Kruse]]
Tags: #Fuzzy_Logic, #academic_papers
Read on: [[October 31st, 2020]]
URL: https://www.researchgate.net/publication/221000724_NEFCLASS_-_a_neuro-fuzzy_approach_for_the_classification_of_data
# Main Contribution(s)
- Proposes [[NEFCLASS (Architecture)]], a neuro-fuzzy system for the classification of data, which is extended from a fuzzy perceptron. 
# Summary
- [[Fuzzy Perceptron]] has weights modelled as fuzzy sets. For example, a 3 layer feedforward neural network $$(U, W, \text{NET}, A, O, ex)$$ where
- $$U = \cup_{i\in M} U_i$$, a non-empty set of neurons and $$M = {1,2,3}$$
- $$W : U \times U \rightarrow F(R)$$ such that there are only connections $$W(u,v)$$ with $$u \in U_i, v \in U_{i+1} (i \in \{1,2\})$$
- $$A$$, an activation function
- $$O$$, an output function
- $$\text{NET}$$, a propagation function to calculate the net input
- $$\text{ex}: U_1 \rightarrow R$$ which only is defined for each input unit
- [[NEFCLASS (Architecture)]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FnsvjTC8nf7.png?alt=media&token=7e6882a9-b1c7-407e-a63e-8eefdabf77c4)
- Main feature are the shared weights on some connections
- Two ways of creating a model
- A system created from scratch starts with no hidden units at all. A rule is created by finding an input pattern p the combination of fuzzy sets, where each yields the highest degree of membership for the respective input feature.
- We can also instead use a scoring system with an unlimited number of rules, then prune the lower rules with lower scores
- Rule learning algorithm
            1. Select next pattern from task
            2. For each input unit, find the membership function such 
            3. If there are still less than $$k_max$$ rule nodes, and there is no rule node $$R$$ with $$W(x_1, R) = \mu_{j1}^{(1)},..., W(x_n, R) = \mu_{jn}^{(n)}$$, then create such a node, and connect it to the output node
            4. If there are still unprocessed patterns, and $$k < k_max$$, then repeat from step (i), and stop otherwise
- Fuzzy set learning algorithm
            1. Select next pattern from task, propagate through system, determine output vector
            2. For each output unit, determine delta value 
            3. For each rule
    - Determine the delta value
    - Find $$x^{\prime}$$
    - For the fuzzy set $$W(x^{\prime}, R)$$, determine delta values for its parameters $$a,b,c$$, using the learning rate $$\alpha >0$$
            4. If an epoch is completed, and the end criterion reached, then stop. Otherwise repeat from (i)
- For [[IRIS dataset]], increasing number of hidden units usually did not produce a better result.
# Learning Gaps/Thoughts
# Simplify/Analogies
